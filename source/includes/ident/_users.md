# Users

## List Users

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users
HTTP/2 200
```

> Response JSON:

```json
[
  {
        "id": "7fc90f5a-45e3-42ed-84b9-c13aed6481f1",
        "created_at": "2018-10-09T02:29:30.580961Z",
        "name": "EntArchitect",
        "email": "big-arch@example.com"
    },
    {
        "id": "876e4fc6-b379-432c-8f76-7e42a955d527",
        "created_at": "2018-10-09T02:21:14.531578Z",
        "name": "SavvyExec",
        "email": "vip@example.com"
    }
]
```

List `User`s for the authorized `Application`.


## Create User

```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users \
    -d '{"name": "Vitalik Buterin", "email": "vitalik@example.com", password": "3sWWKn7jQhbj#XW5CXTappB!E6WzwZuc"}'
HTTP/2 201
```
> Response JSON:

```json
[
  {
    "id": "876e4fc6-b379-432c-8f76-7e42a955d527",
    "created_at": "2018-10-09T02:21:14.531577683Z",
    "name": "Vitalik Buterin",
    "email": "vitalik@example.com"
  }
]
```

Create a new platform `User` or a `User` on behalf of an authorized `Application`.

### Request Parameters

Parameter | Description
--------- | -----------
name | full name of the `User`
email | email address for the `User`; must be capable of receiving email at time of creation
application_id | id of the `Application` with which the `User` will be associated


## Update User

```shell
curl -i -XPUT \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/users/876e4fc6-b379-432c-8f76-7e42a955d527 \
    -d '{"password": "the new password"}'
HTTP/2 204
```

Update an existing `User`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `User`


## Delete a User

<i>Documentation forthcoming.</i>

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `User`


## List User KYC Applications

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/users/876e4fc6-b379-432c-8f76-7e42a955d527/kyc_applications
HTTP/2 200
```

> Response JSON:

```json
[
  {
    "id": "5286091c-a6ea-4546-9212-9c50925289f3",
    "created_at": "2019-06-04T14:53:34.497081-04:00",
    "application_id": null,
    "user_id": "876e4fc6-b379-432c-8f76-7e42a955d527",
    "provider": "identitymind",
    "identifier": "3d03c423f58747da9ced20bfee199975",
    "type": "kyc",
    "status": "accepted",
    "params": {
        "man": "Vitalik Buterin",
        "tid": "3d03c423f58747da9ced20bfee199975"
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
                            "ts": 1559889000000
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
        "mtid": "9d26c9dbb0174f38b57d76091b979928",
        "rcd": "",
        "state": "A",
        "tid": "9d26c9dbb0174f38b57d76091b979928"
    }
  }
]
```

List `KYCApplication`s associated with a `User`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `User`
