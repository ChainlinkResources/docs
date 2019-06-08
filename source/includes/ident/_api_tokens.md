# API Tokens

## List API Tokens

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/tokens
HTTP/2 200
```

> Response JSON:

```json
[
  {
        "id": "234da41d-0970-4561-bdf9-797ef6807fb5",
        "created_at": "2018-10-08T23:34:18.843828Z",
        "issued_at": "2018-10-08T23:34:18.842733Z",
        "expires_at": null,
        "token": "a-New-toKeN-VaLuE",
        "data": null
    },
    {
        "id": "84557020-0180-4e87-ae01-ffa05a587df4",
        "created_at": "2018-10-08T23:58:28.631901Z",
        "issued_at": "2018-10-08T23:58:28.630644Z",
        "expires_at": null,
        "token": "anOthEr-New-toKeN-VaLuE",
        "data": null
    }
]
```

This endpoint enumerates previously authorized Tokens for the authorized User or Application.


## Create API Token

```shell
curl -i -XPOST \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://ident.provide.services/api/v1/tokens \
    -d '{"name": "PurposeToken"}'
HTTP/2 201
```

> Response JSON:

```json
[
  {
    "id": "ed3d83ec-8b4f-4538-a240-bf759a2545ff",
    "created_at": "2018-10-09T02:47:25.981937848Z",
    "issued_at": "2018-10-09T02:47:25.980910555Z",
    "expires_at": null,
    "token": "a-New-toKeN-VaLuE",
    "data": null
}
]
```

This endpoint authorizes a `Token` on behalf of a `User` or `Application`.


## Delete API Token

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/tokens/84557020-0180-4e87-ae01-ffa05a587df4
HTTP/2 204
```

This endpoint destroys a previously authorized `Token` on behalf of the authorized `User` or `Application`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Token`
