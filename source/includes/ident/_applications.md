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
        "id": "b8afffd7-cb0a-49b4-bb61-fac83ce9673e",
        "created_at": "2019-06-07T09:04:16.500210244Z",
        "network_id": "aa51a87f-f142-4341-8e94-b4b0214a009f",
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "Provide Payments",
        "description": null,
        "config": null,
        "hidden": false
    }
]
```

List platform `Application`s visible to the authorized `User`.

### Query Parameters

Parameter | Default | Description
--------- | ----- | -----------
hidden | `false` | flag to indicate if hidden `Application`s should be filtered
network_id | n/a | id of the `Network` for which the `Application`s should be filtered


## Create Application

```shell
curl -i -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NjAwNTg0NTksImp0aSI6IjU0YWZmMGQ1LTFjY2ItNDRmNy1iYTRiLTExYTA3YWFhZGM2YiIsInN1YiI6InVzZXI6NTE4MzE5MmQtYWM4NS00YzVhLWE3OGQtODAzMWE4ZDIwODc4In0.jI7S0gW__iFjbZi0o8AKyqrH8D01vpCpgV3HOh9TrUE' \
    https://ident.provide.services/api/v1/applications \
    -d '{
    "config":{
        "network_id":"ef976635-545b-46c6-9576-4e3a893a68e9"
    },
    "name":"providepayments"
}'
HTTP/2 201
```

> Response JSON:

```json
{
    "id": "0a032196-5e9d-4aa0-afd7-a7e66dd2b963",
    "created_at": "2019-06-09T01:35:13.044603-04:00",
    "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
    "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
    "name": "providepayments",
    "description": null,
    "config": null,
    "hidden": false
}
```

Creates a new logical `Application` on behalf of the authorized platform `User`.

### Request Parameters

Parameter | Description
--------- | -----------
name | name of the `Application`
network_id | id of the `Network` where `Application` resources will be deployed


## Retrieve Application details

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications/b8afffd7-cb0a-49b4-bb61-fac83ce9673e
HTTP/2 200
```

> Response JSON:

```json
[
    {
        "id": "b8afffd7-cb0a-49b4-bb61-fac83ce9673e",
        "created_at": "2019-06-07T09:04:16.500210244Z",
        "network_id": "aa51a87f-f142-4341-8e94-b4b0214a009f",
        "user_id": "40bc70bf-1140-4978-99bc-b8b800672842",
        "name": "Provide Payments",
        "description": null,
        "config": null,
        "hidden": false
    }
]
```

Retrieve details for an `Application`.

### Query Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`


## Update Application

```shell
curl -i -XPUT \
    -H 'content-type: application/json' \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications/b8afffd7-cb0a-49b4-bb61-fac83ce9673e \
    -d '{"enabled": false}'
HTTP/2 204
```

Update an `Application`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`


## List Application Tokens

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

List `Token`s associated with the specified `Application`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`
