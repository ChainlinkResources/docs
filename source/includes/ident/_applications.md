# Applications

## List Applications

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://ident.provide.services/api/v1/applications
HTTP/2 200
date: Sun, 09 Jun 2019 04:58:25 GMT
content-length: 872
content-type: application/json; charset=UTF-8
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
x-total-results-count: 2
```

> Response JSON:

```json
[
    {
        "id": "5c453bea-da24-4123-9b43-d35ded159531",
        "created_at": "2019-06-09T05:32:24.526827-04:00",
        "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
        "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
        "name": "providepayments",
        "description": null,
        "config": {
            "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9"
        },
        "hidden": false
    },
    {
        "id": "3861ef98-332a-4666-b5de-d382c77d481c",
        "created_at": "2019-06-09T05:40:11.911719-04:00",
        "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
        "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
        "name": "Digitized Bill of Lading",
        "description": null,
        "config": {
            "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9"
        },
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
date: Sun, 09 Jun 2019 04:58:25 GMT
content-type: application/json; charset=UTF-8
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
```

> Response JSON:

```json
{
    "id": "acc45205-9043-4174-b349-8ea5aded3685",
    "created_at": "2019-06-09T05:34:09.124485-04:00",
    "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
    "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
    "name": "providepayments",
    "description": null,
    "config": {
        "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9"
    },
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
    https://ident.provide.services/api/v1/applications/acc45205-9043-4174-b349-8ea5aded3685
HTTP/2 200
date: Sun, 09 Jun 2019 04:58:25 GMT
content-length: 380
content-type: application/json; charset=UTF-8
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count

```

> Response JSON:

```json
{
    "id": "acc45205-9043-4174-b349-8ea5aded3685",
    "created_at": "2019-06-09T05:34:09.124485-04:00",
    "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
    "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
    "name": "providepayments",
    "description": null,
    "config": {
        "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9"
    },
    "hidden": true
}
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
    https://ident.provide.services/api/v1/applications/acc45205-9043-4174-b349-8ea5aded3685 \
    -d '{"hidden": true}'
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
    https://ident.provide.services/api/v1/applications/acc45205-9043-4174-b349-8ea5aded3685/tokens
HTTP/2 200
date: Sun, 09 Jun 2019 09:41:26 GMT
content-length: 523
content-type: application/json; charset=UTF-8
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
x-total-results-count: 1
```

> Response JSON:

```json
[
    {
        "id": "dff4470f-69ae-47c7-96d3-409fe83aa2f9",
        "created_at": "2019-06-09T05:34:09.129953-04:00",
        "issued_at": "2019-06-09T05:34:09.12981-04:00",
        "expires_at": null,
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NjAwNzI4NDksImp0aSI6ImRmZjQ0NzBmLTY5YWUtNDdjNy05NmQzLTQwOWZlODNhYTJmOSIsInN1YiI6ImFwcGxpY2F0aW9uOmFjYzQ1MjA1LTkwNDMtNDE3NC1iMzQ5LThlYTVhZGVkMzY4NSJ9.Nrwb6yRqYn4TJC-j_xIN9PFoAG5ap63SYkykmuY-MAA",
        "data": null
    }
]
```

List `Token`s associated with the specified `Application`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Application`
