# Oracles

## List Oracles

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/oracles
HTTP/2 200
```

> Response JSON:


This endpoint enumerates managed oracle contracts.


### HTTP Request

`GET /api/v1/oracles`


## Create and deploy an Oracle


This endpoint creates a managed Oracle smart contract and deploys it to a Network. Upon successful deployment, the data feed will be consumed and written onto the ledger associated with the Network.

<i> (Not yet implemented)</i>

### HTTP Request

`POST /api/v1/oracles`


## Get a Specific Oracle


This endpoint retrieves details for a specific oracle.


### HTTP Request

`GET /api/v1/oracles/:id`

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the Oracle
