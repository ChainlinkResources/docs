# KYC

Provide has built a KYC service which acts as an API gateway to third-party digital identity management platforms in an effort to create a standard, developer-friendly way to interact with digital signing identities in the context of KYC (and KYB), AML compliance and fraud prevention. We are open to adding support for additional third-party KYC/AML API providers. If you would like to see us add support for a new provider, please [contact us](https://provide.services/contact-us).

The KYC API gateway acts as a passthrough to a configured third-party API (the `provider`). Provide manages the KYC/KYB application lifecycle to help your compliance department perform remediation. Upon submission of a KYC (or KYB) application, the platform asyncronously monitors the application for state changes; subscriptions can be configured to notify your application when manual remediation is required. More details on these notifications will be provided in a subsequent update to this documentation.

## Third-Party API Support

Provide's KYC service currently supports the following third-party vendors:

Name | KYC Application Provider | API Reference
--------- | ----------- | -----------
IdentityMind | `identitymind` | <a href="https://edoc.identitymind.com/reference" target="_blank">https://edoc.identitymind.com/reference</a>
Vouched | `vouched` | <a href="https://docs.vouched.id" target="_blank">https://docs.vouched.id</a>

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
        "description":"No national id country specified, and invalid format for US Social Security Number",
        "params":null,
        "provider_representation":null
    },
    {
        "id":"9dc4c2e1-b651-41bf-b67f-3bed255990d0",
        "created_at":"2019-06-12T02:30:52.519887-04:00",
        "application_id":"bca2348c-442f-4c48-99a4-7b3510385e53",
        "user_id":"47069619-2035-4193-bdd0-af4d5096b649",
        "provider":"identitymind",
        "identifier":"880c4ba7877d43c09c70f0ca89ea1e17",
        "type":"kyc",
        "status":"accepted",
        "description":null,
        "params":null,
        "provider_representation":null
    },
    {
        "id":"c95fbbce-dd1b-46ee-a147-4c324dfbccd8",
        "created_at":"2019-06-12T02:27:17.393292-04:00",
        "application_id":"bca2348c-442f-4c48-99a4-7b3510385e53",
        "user_id":"47069619-2035-4193-bdd0-af4d5096b649",
        "provider":"identitymind",
        "identifier":"4ab49de247bc44ec864434163ec1fe2e",
        "type":"kyc",
        "status":"accepted",
        "description":null,
        "params":null,
        "provider_representation":null
    }
]
```

List KYC applications visible to the authorized User or Application.


## Create KYC Application

```shell
curl -i -XPUT \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/1bd7e730-67e5-4418-b624-c0c47b072f8b \
    -d '{"params":{"man": "Joe Lubin", "tea": "joe@example.com"}}'
HTTP/2 202
```

> Response JSON:

```json
{
    "id":"1bd7e730-67e5-4418-b624-c0c47b072f8b",
    "created_at":"2019-06-07T02:30:00.115517-04:00",
    "application_id":null,
    "user_id":"00d4adc9-b0ca-4c94-9d90-3c61f696b8bd",
    "provider":"identitymind",
    "identifier":"95ed799287ee48ccadf4cf1f654e064c",
    "type":"kyc",
    "status":"submitted",
    "description":null,
    "params":{
        "man":"Joe Lubin",
        "tea":"joe@example.com"
    },
    "provider_representation":{
        "ednaScoreCard":{
            "er":{
                "profile":"DEFAULT",
                "reportedRule":{
                    "description":"Rule fired from sandbox",
                    "details":"[Fired] details",
                    "name":"Sandbox Rule",
                    "resultCode":"ACCEPT",
                    "ruleId":1002,
                    "testResults":[
                        {
                            "condition":{
                                "left":"ed:1",
                                "operator":"eq",
                                "right":true
                            },
                            "details":"[Fired] details",
                            "fired":true,
                            "stage":"1",
                            "test":"ed:1",
                            "ts":1559891359000
                        }
                    ]
                }
            },
            "etr":[
                {
                    "details":"true",
                    "test":"ed:20"
                },
                {
                    "details":"true",
                    "test":"ed:31"
                },
                {
                    "details":"true",
                    "test":"ed:2"
                },
                {
                    "details":"true",
                    "test":"ed:1"
                },
                {
                    "details":"true",
                    "test":"ed:28"
                }
            ],
            "sc":[
                {
                    "details":"true",
                    "test":"ed:1"
                }
            ]
        },
        "erd":"Unknown User",
        "frd":"[Fired] details",
        "frn":"Sandbox Rule",
        "frp":"ACCEPT",
        "mtid":"95ed799287ee48ccadf4cf1f654e064c",
        "rcd":"131,101,50005,150,202,1002",
        "res":"ACCEPT",
        "state":"A",
        "tid":"95ed799287ee48ccadf4cf1f654e064c",
        "upr":"UNKNOWN",
        "user":"UNKNOWN"
    }
}
```

Create a KYC application using the specified third-party provider.

### Request Parameters

Name | Type | Default | Description
--------- | ----------- | ----------- | -----------
provider | string | `"identitymind"` | third-party KYC provider; delegate to whom the KYC API gateway will passthrough `params`
params | object | `nil` | KYC application parameters specific to the third-party `provider`
type | string | `"kyc"` | KYC application type (`kyc` or `kyb`)
status | string | `"pending"` | the status of the KYC application; must be a valid state transition in the context of the application's current state

For `provider`-specific `params` reference, please see [Third-Party API Support](#third-party-api-support).


## Update KYC Application

```shell
curl -i -XPUT \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/1bd7e730-67e5-4418-b624-c0c47b072f8b \
    -d '{"params":{"man": "Joe Lubin", "tea": "joe@example.com"}}'
HTTP/2 202
```

> Response JSON:

```json
{
    "id": "1bd7e730-67e5-4418-b624-c0c47b072f8b",
    "created_at": "2019-06-07T02:30:00.115517-04:00",
    "application_id": null,
    "user_id": "00d4adc9-b0ca-4c94-9d90-3c61f696b8bd",
    "provider": "identitymind",
    "identifier": "95ed799287ee48ccadf4cf1f654e064c",
    "type": "kyc",
    "status": "submitted",
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
        "erd": "Unknown User",
        "frd": "[Fired] details",
        "frn": "Sandbox Rule",
        "frp": "ACCEPT",
        "mtid": "95ed799287ee48ccadf4cf1f654e064c",
        "rcd": "131,101,50005,150,202,1002",
        "res": "ACCEPT",
        "state": "A",
        "tid": "95ed799287ee48ccadf4cf1f654e064c",
        "upr": "UNKNOWN",
        "user": "UNKNOWN"
    }
}
```

Update a previously submitted KYC application and asynchronously resubmit it to the third-party `provider` on behalf of the authorized `User` or `Application`.

### Request Parameters

Name | Type | Description
--------- | ----------- | -----------
provider | string | third-party KYC provider; delegate to whom the KYC API gateway will passthrough `params`
params | object | KYC application parameters specific to the third-party `provider`
type | string | KYC application type (`kyc` or `kyb`)
status | string | the status of the KYC application; must be a valid state transition in the context of the application's current state

For `provider`-specific `params` reference, please see [Third-Party API Support](#third-party-api-support).

### KYC Application Status & Accepting or Rejecting a KYC Application

The `status` parameter represents the current status of the KYC application; the following are valid `status` values:

Value | Description
--------- | -----------
accepted | the KYC application was accepted
failed | the KYC application submission to the third-party `provider` failed
pending | the KYC application has not yet been submitted to the third-party `provider`
rejected | the KYC application was rejected
submitted | the KYC application has been submitted to the third-party `provider` but no decision has been resolved
review | the KYC application is under review


## Retrieve KYC Application Details

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/kyc_applications/1bd7e730-67e5-4418-b624-c0c47b072f8b
HTTP/2 200
```

> Response JSON:

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
