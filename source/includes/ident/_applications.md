# Applications

## List Applications

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications
HTTP/2 200
```

> Response JSON:

```json
[
  {
        "id": "cf6ae66a-7cba-48ce-bbd5-9dcd674267be",
        "created_at": "2018-10-09T01:28:52.704799Z",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "Enterprise Advantage",
        "description": null,
        "config": {
            "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4"
        },
        "hidden": false
    },
    {
        "id": "6fd50c17-0d3f-463f-811e-0015e0373f1a",
        "created_at": "2018-10-09T01:30:05.575747Z",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "Process Turbo",
        "description": null,
        "config": {
            "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4"
        },
        "hidden": false
    }
]
```

This endpoint enumerates platform Applications visible to the authorized caller.

### HTTP Request

`GET /api/v1/applications`

## Create an Application

```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications \
    -d '{"name": "SavvyApp"}'
HTTP/2 201
```


> Response JSON:

```json
[
  {
    "id": "77cb2094-9a99-4de6-ac86-bbd2353b49c8",
    "created_at": "2018-10-09T02:03:19.617250119Z",
    "network_id": "00000000-0000-0000-0000-000000000000",
    "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
    "name": "SavvyExec",
    "description": null,
    "config": null,
    "hidden": false
}
]
```

This endpoint creates a new Application on behalf of the authorized platform User.

### HTTP Request

`POST /api/v1/applications`

## Get Application details


```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications/cf6ae66a-7cba-48ce-bbd5-9dcd674267be
HTTP/2 200
```


> Response JSON:

```json
[
  {
    "id": "cf6ae66a-7cba-48ce-bbd5-9dcd674267be",
    "created_at": "2018-10-09T01:28:52.704799Z",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
    "name": "Enterprise Advantage",
    "description": null,
    "config": {
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4"
    },
    "hidden": false
}
]
```

This endpoint retrieves the details of the specified Application.

### HTTP Request

`GET /api/vi/applications/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`


## Update Application details


```shell
curl -i -XPUT \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications/6fd50c17-0d3f-463f-811e-0015e0373f1a \
    -d '{"name": "Turbo Process"}'
HTTP/2 204
```

This endpoint updates details of the specified Application.

### HTTP Request

`PUT /api/vi/applications/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`


## Get Application tokens

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications/cf6ae66a-7cba-48ce-bbd5-9dcd674267be/tokens
HTTP/2 200
```


> Response JSON:

```json
[
    {
        "id": "ba562b25-ff4e-4f9d-a332-31550ead9f41",
        "created_at": "2018-10-09T01:28:52.726631Z",
        "issued_at": "2018-10-09T01:28:52.725677Z",
        "expires_at": null,
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE",
        "data": null
    }
]
```

This endpoint fetches the Tokens of the specified Application.

### HTTP Request

`GET /api/vi/applications/:id/tokens`

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`

## Delete an Application


```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications/77cb2094-9a99-4de6-ac86-bbd2353b49c8
HTTP/2 501
```


> Response JSON:

```json
[
  {
    "message": "not implemented"
}
]
```

This endpoint removes the specified Application.

<i>(Not yet implemented)</i>

### HTTP Request

`DELETE /api/vi/applications/:id`

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`