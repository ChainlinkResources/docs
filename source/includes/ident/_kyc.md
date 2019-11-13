# KYC

Provide has built a KYC service which acts as an API gateway to third-party digital identity management platforms in an effort to create a standard, developer-friendly way to interact with digital signing identities in the context of KYC (and KYB), AML compliance and fraud prevention. The KYC API gateway allows applications to conform to an upstream partner's compliance requirements without compromising the UX of their own applications. We are open to adding support for additional third-party KYC/AML API providers. If you would like to see us add support for a new provider, please [contact us](https://provide.services/contact-us).

The KYC API gateway acts as a passthrough to a configured third-party API (the `provider`). Provide manages the KYC/KYB application lifecycle to help your compliance department perform remediation. Upon submission of a KYC (or KYB) application, the platform asyncronously monitors the application for state changes; subscriptions can be configured to notify your application when manual remediation is required. More details on these notifications will be provided in a subsequent update to this documentation.

## Third-Party API Support

Provide's KYC service currently supports the following third-party vendors:

Name | KYC Application Provider | API Reference
--------- | ----------- | -----------
IdentityMind | `identitymind` | <a href="https://edoc.identitymind.com/reference" target="_blank">https://edoc.identitymind.com/reference</a>
Vouched | `vouched` | <a href="https://docs.vouched.id" target="_blank">https://docs.vouched.id</a>

## Webhook Support

The Provide KYC API gateway implements fault-tolerant KYC remediation. When the status of a KYC application changes, your application can be configured to receive notifications at a configured HTTP `webhook_url`. Webhook notifications requests sent to this URL include a signature in the `X-Request-Signature` header. This allows you to verify that the requests were sent by Provide and not by a third party. Signatures can only be verified manually at this time as described below.

### Preventing replay attacks

A replay attack is when an attacker intercepts a valid payload and its signature and retransmits them. To mitigate such attacks, Provide includes a timestamp in the `X-Request-Signature` header. Because this timestamp is also part of the signed payload, it is verified by the signature. An attacker cannot change the timestamp without invalidating the signature. If the signature is valid but the timestamp is too old, you can have your application reject the payload at your discretion.

We recommend that you use Network Time Protocol (NTP) to ensure that your server's clock is accurate and synchronizes with the time on Provide's servers.

Provide generates the timestamp and signature each time we send an notification to your endpoint. If a notification is retried (i.e., in the event your configured endpoint previously issued a non-2xx response), then a new signature and timestamp is generated for the retry attempt.

### Verifying signatures

We may release webhook signature verification examples using one of our official libraries in the future. Please use the following instructions to implement signature verification in your configured webhook endpoint.

The `X-Request-Signature` header contains a timestamp and signature. The timestamp and signature are prefixed by `t=` and `s=`, respectively, and comma-delimited.

```shell
X-Request-Signature: t=1257894000,s=5b5e838f593e1bae355109bce56939f5ccae74586635f4f95d68bb6b526c40ac
```

Provide generates signatures using a hash-based message authentication code (<a href="https://en.wikipedia.org/wiki/Hash-based_message_authentication_code" target="_blank">HMAC</a>) with <a href="https://en.wikipedia.org/wiki/SHA-2" target="_blank">SHA-256</a>.

It is not currently possible to have multiple active secrets for generating signatures.

### Step 1: Extract the timestamp and signatures from the header

Split the header, using the `,` character as the delimiter to split on, to get a list of key/value pair strings. Then split each raw string, using the `=` character as the separator, to arrive at each key and its associated value.

The value for the prefix `t` corresponds to the timestamp, and `s` corresponds to the signature.

### Step 2: Generate the signed payload string

You achieve this by concatenating:

- The timestamp (as a string)
- The character `.`
- The raw JSON payload (i.e., the request body)

### Step 3: Determine the expected signature

Compute an HMAC with the SHA-256 hash function. Use the application's signing secret as the key, and use the signed payload string generated in step (2) above as the message.

### Step 4: Compare signatures

Compare the signature in the header to the expected signature. If the signatures match, compute the difference between the current and received timestamps. It is up to you to determine if the difference is within your tolerance. A higher tolerance is more susceptible to replay attaacks.

To protect against timing attacks, use a constant-time string comparison to compare the expected signature to the received signature.

## List KYC Applications

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications
HTTP/2 200
date: Wed, 12 Jun 2019 05:39:19 GMT
content-type: application/json; charset=UTF-8
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
x-total-results-count: 3
```

> Response JSON:

```json
[
    {
        "id":"72258a99-1518-4526-a5fa-043081eee7f0",
        "created_at":"2019-06-12T02:31:33.613098-04:00",
        "application_id":"bca2348c-442f-4c48-99a4-7b3510385e53",
        "user_id":"47069619-2035-4193-bdd0-af4d5096b649",
        "provider":"identitymind",
        "identifier":null,
        "type":"kyc",
        "status":"failed",
        "name":"Tim Evans",
        "description":"No national id country specified, and invalid format for US Social Security Number",
    },
    {
        "id":"13bd0b24-f0d9-4caa-89ab-259c058877ce",
        "created_at":"2019-11-13T03:55:02.687098-05:00",
        "application_id":"dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "user_id":"9a253758-197a-4308-8d2d-61cfe9317644",
        "provider":"vouched",
        "identifier":"OsccQPWf",
        "type":"kyc",
        "status":"remediate",
        "name":"John Smith",
        "description": null
    },
    {
        "id":"e40a34d8-5df9-4ab3-be79-b8b34844eb3d",
        "created_at":"2019-11-05T22:23:31.126578-05:00",
        "application_id":"dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "user_id":"3fceea52-b71c-4b7f-bb88-712046523310",
        "provider":"vouched",
        "identifier":"oRM3YnSy",
        "type":"kyc",
        "status":"accepted",
        "name":"Joe Lubin",
        "description": null
    }
]
```

List KYC applications visible to the authorized User or Application.


## Create KYC Application

```shell
curl -i -XPUT \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/1bd7e730-67e5-4418-b624-c0c47b072f8b \
    -d '{
    "user_id": "00d4adc9-b0ca-4c94-9d90-3c61f696b8bd",
    "provider": "vouched",
    "params": {
        "type": "id-verification",
        "webhook_url": "https://url.to.my/webhook",
        "date_of_birth": "1988-10-01",
        "first_name": "John",
        "last_name": "Smith",
        "id_photo": "<base64-encoded image data>",
        "id_photo_back": "<base64-encoded image data>",
        "selfie": "<base64-encoded image data>",
    }
}'
HTTP/2 201
```

> Response JSON:

```json
{
  "id": "205d1f45-4b45-4d85-a692-8db40d94ab89",
  "created_at": "2019-11-13T04:24:48.241681-05:00",
  "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
  "user_id": "00d4adc9-b0ca-4c94-9d90-3c61f696b8bd",
  "provider": "vouched",
  "identifier": null,
  "type": "kyc",
  "status": "pending",
  "name": "John Smith",
  "description": null,
  "params": {
      "date_of_birth": "1988-10-01",
      "first_name": "John",
      "last_name": "Smith",
      "id_photo": "<base64-encoded image data>",
      "id_photo_back": "<base64-encoded image data>",
      "selfie": "<base64-encoded image data>",
      "type": "id-verification",
      "webhook_url": "https://url.to.my/webhook"
    }
}
```

Create a KYC application using the specified third-party provider.

### Request Parameters

Name | Type | Default | Description
--------- | ----------- | ----------- | -----------
provider | string | `vouched` | third-party KYC provider; delegate to which the API gateway will dispatch the KYC or KYB application
params | object | `nil` | KYC application parameters, normalized for generic use with any supported `provider`; a nested `params` object, if included within this parameter, is completely passed through to the third-party `provider` API
type | string | KYC application type (`kyc` or `kyb`)
user_id | uuid | `kyc` | id of the `User` which is the subject of the KYC application; this parameter is only relevant if calling the API on behalf of an `Application`

For `provider`-specific `params` reference, please see [Third-Party API Support](#third-party-api-support).


## Update KYC Application

```shell
curl -i -XPUT \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/1bd7e730-67e5-4418-b624-c0c47b072f8b \
    -d '{
    "status": "accepted"
}'
HTTP/2 202
```

> Response JSON:

```json
{
    "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
    "created_at": "2019-11-13T04:24:48.241681-05:00",
    "description": null,
    "id": "205d1f45-4b45-4d85-a692-8db40d94ab89",
    "identifier": "VS5eRURs",
    "name": "Truong Tri Tung",
    "provider": "vouched",
    "status": "accepted",
    "type": "kyc",
    "user_id": "9a253758-197a-4308-8d2d-61cfe9317644",
}
```

Update a previously submitted KYC application and asynchronously resubmit it to the third-party `provider` on behalf of the authorized `User` or `Application`.

### Request Parameters

Name | Type | Description
--------- | ----------- | -----------
status | string | the status of the KYC application; must be a valid state transition in the context of the application's current state

For `provider`-specific `params` reference, please see [Third-Party API Support](#third-party-api-support).

### KYC Application Status & Accepting or Rejecting a KYC Application

The `status` parameter represents the current status of the KYC application; the following are valid `status` values:

Value | Description
--------- | -----------
accepted | the KYC application was accepted
failed | the KYC application submission to the third-party `provider` failed
pending | the KYC application is in the process of being submitted to the third-party `provider`
rejected | the KYC application was rejected, either by the third-party `provider` AI, or manually by way of remediation
remediate | the KYC application requires remediation due to its similarity with another KYC application or other risk factors
review | the KYC application has been submitted to the third-party `provider` and is currently being processed
submitted | the KYC application has been submitted to the third-party `provider` but no decision has been resolved


## Retrieve KYC Application Details

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/1bd7e730-67e5-4418-b624-c0c47b072f8b
HTTP/2 200
```

> Response JSON (Identitymind provider):

```json
{
    "id": "1bd7e730-67e5-4418-b624-c0c47b072f8b",
    "created_at": "2019-06-07T02:30:00.115517-04:00",
    "application_id": null,
    "user_id": "00d4adc9-b0ca-4c94-9d90-3c61f696b8bd",
    "provider": "identitymind",
    "identifier": "95ed799287ee48ccadf4cf1f654e064c",
    "type": "kyc",
    "status": "accepted",
    "description":null,
    "params": {
        "man": "Joe Lubin",
        "tea": "joe@example.com"
    },
    "provider_representation": {
        "ednaScoreCard": {
            "er": {
                "profile": "DEFAULT",
                "reportedRule": {
                    "description": "Rule fired from sandbox",
                    "details": "[Fired] details",
                    "name": "Sandbox Rule",
                    "resultCode": "ACCEPT",
                    "ruleId": 1002,
                    "testResults": [
                        {
                            "condition": {
                                "left": "ed:1",
                                "operator": "eq",
                                "right": true
                            },
                            "details": "[Fired] details",
                            "fired": true,
                            "stage": "1",
                            "test": "ed:1",
                            "ts": 1559891359000
                        }
                    ]
                }
            },
            "etr": [
                {
                    "details": "true",
                    "test": "ed:20"
                },
                {
                    "details": "true",
                    "test": "ed:31"
                },
                {
                    "details": "true",
                    "test": "ed:2"
                },
                {
                    "details": "true",
                    "test": "ed:1"
                },
                {
                    "details": "true",
                    "test": "ed:28"
                }
            ],
            "sc": [
                {
                    "details": "true",
                    "test": "ed:1"
                }
            ]
        },
        "mtid": "95ed799287ee48ccadf4cf1f654e064c",
        "rcd": "",
        "state": "A",
        "tid": "95ed799287ee48ccadf4cf1f654e064c"
    }
}
```

> Response JSON (Vouched provider):

```json
{
  "id": "e494ee10-bbf5-45bb-81aa-7e3561d8c729",
  "created_at": "2019-09-15T02:42:00.743047-04:00",
  "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
  "user_id": "9e15791a-dbf1-4e5e-8c6b-a7253e198b4c",
  "provider": "vouched",
  "identifier": "hDj_HOv",
  "type": "kyc",
  "status": "submitted",
  "description": null,
  "params": {
    "params": {
        "date_of_birth": "06/22/1990",
        "first_name": "Janice",
        "last_name": "Way",
        "id_photo": "<base64-encoded image data>",
        "id_photo_back": "<base64-encoded image data>",
        "selfie": "<base64-encoded image data>",
        "type": "id-verification",
        "webhook_url": 
    },
    "type": "id-verification"
  },
  "provider_representation": {
    "errors": [
      {
        "message": "Invalid or unsupported id",
        "suggestion": null,
        "type": "InvalidIdPhotoError"
      },
      {
        "message": "Invalid or unsupported selfie",
        "suggestion": null,
        "type": "InvalidUserPhotoError"
      },
      {
        "message": "Id and selfie faces do not match",
        "suggestion": null,
        "type": "FaceMatchError"
      },
      {
        "message": "Name is below the confidence threshold",
        "suggestion": null,
        "type": "NameMatchError"
      },
      {
        "message": "Birth date is below the confidence threshold",
        "suggestion": null,
        "type": "BirthDateMatchError"
      }
    ],
    "id": "hDj_HOv",
    "request": {
      "callbackURL": "https://google.com/gdpr",
      "parameters": {
        "carInsurancePhoto": null,
        "dob": "06/22/1990",
        "dotPhoto": null,
        "firstName": "Janice",
        "idPhoto": "<base64-encoded image data>",
        "idPhotoBack": null,
        "lastName": "Way",
        "twicPhoto": null,
        "userPhoto": "<base64-encoded image data>"
      },
      "type": "id-verification"
    },
    "result": {
      "confidences": {
        "backId": null,
        "faceMatch": 0,
        "id": 0.4327,
        "idMatch": 0,
        "selfie": 0.0434
      },
      "country": "US",
      "dob": null,
      "errors": null,
      "firstName": null,
      "id": null,
      "lastName": null,
      "state": "WI",
      "success": false,
      "type": "drivers-license"
    },
    "status": "completed",
    "submitted": "2019-09-15T06:42:02+00:00"
  }
}
```

Retrieve a previously submitted KYC application and enrich it with the latest third-party representation. This is useful to check the remediation status of an application.


## Upload KYC Application Document

```shell
curl -i -XPOST \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/5286091c-a6ea-4546-9212-9c50925289f3/documents \
    -d '{}'
HTTP/2 202
```

> Response JSON:

```json
{}
```

Upload and attach a document to an existing KYC application.

<i>Documentation forthcoming.</i>


## List KYC Application Documents

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/5286091c-a6ea-4546-9212-9c50925289f3/documents
HTTP/2 200
```

> Response JSON:

```json
[
    {}
]
```

List documents attached to a KYC application.

<i>Documentation forthcoming.</i>

## Download KYC Application Document

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/5286091c-a6ea-4546-9212-9c50925289f3/documents
HTTP/2 200
```

> Response JSON:

```json
[
    {}
]
```

Download a document attached to a KYC application.

<i>Documentation forthcoming.</i>
