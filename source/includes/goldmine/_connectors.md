# Connectors

## List Connectors

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/connectors
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "9e5e269a-f074-49e2-8383-ab94a33ae30a",
        "created_at": "2018-10-15T03:18:07.942554Z",
        "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "name": "ABC Corp Private IPFS Endpoint",
        "type": "ipfs",
        "config": {
            "gateway_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:8080",
            "rpc_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:5001"
        },
        "accessed_at": null
    }
```

This endpoint enumerates configured Connectors.




## Configure a new Connector

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/applications/25b6339c-f11f-4a00-94d7-0a6e9b64586d/connectors \
    -d '{"network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
          "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
          "type": "ipfs",
          "name": "ABC Corp Private IPFS Endpoint",
          "config": {
            "gateway_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:8080",
            "rpc_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:5001"
          }
        }'
HTTP/2 201
```

> Response JSON:

```json
{
  "id": "9e5e269a-f074-49e2-8383-ab94a33ae30a",
  "created_at": "2018-10-15T03:18:07.942553712Z",
  "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
  "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
  "name": "ABC Corp Private IPFS Endpoint",
  "type": "ipfs",
  "config": {
    "gateway_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:8080",
    "rpc_url": "http://ec2-54-175-49-39.compute-1.amazonaws.com:5001"
  },
  "accessed_at": null
}
```

This endpoint configures a new Connector.





## Retrieve a Connector

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/connectors/9e5e269a-f074-49e2-8383-ab94a33ae30a
HTTP/2 501
```

> Response JSON:

```json
{
    "message": "not implemented"
}
```

This endpoint retrieves the details for the specified Connector.

<i> (Not yet implemented) </i>



### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## Delete a Specific Connector

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/connectors/9e5e269a-f074-49e2-8383-ab94a33ae30a
HTTP/2 204
```


This endpoint removes the specified Connector.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the connector
