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
[
  {
    "id":"e7ceec61-dae7-4697-aa5a-a6868fbb89ca",
    "created_at":"2019-09-17T16:03:35.397391-04:00",
    "application_id":"a1ed9f4b-0770-44d5-a5e5-c9625fe3480f",
    "network_id":"aa51a87f-f142-4341-8e94-b4b0214a009f",
    "name":"IPFS us-east-1",
    "type":"ipfs",
    "status":"init",
    "description":null,
    "config":{
      "api_port":5001,
      "container":"providenetwork-node",
      "gateway_port":8080,
      "provider_id":"docker",
      "region":"us-east-1",
      "role":"peer",
      "security":{
        "egress":"*",
        "ingress":{
          "0.0.0.0/0":{
            "tcp":[
              5001,
              8080
            ],
            "udp":null
          }
        }
      },
      "target_id":"aws"
    },
    "accessed_at":null
  }
]
```

List configured connectors.


## Create Connector

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/applications/25b6339c-f11f-4a00-94d7-0a6e9b64586d/connectors \
    -d '{
          "name":"IPFS us-east-1",
          "network_id":"aa51a87f-f142-4341-8e94-b4b0214a009f",
          "type":"ipfs",
          "config":{
            "region":"us-east-1",
            "target_id":"aws",
            "provider_id":"docker",
            "role":"peer",
            "container":"providenetwork-ipfs",
            "rpc_port":5001,
            "gateway_port":8080,
            "credentials":{
              "aws_access_key_id":"AKIAXXXXXXXXXXXXXXXX",
              "aws_secret_access_key":"XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
            },
            "security":{
              "egress":"*",
              "ingress":{
                "0.0.0.0/0":{
                  "tcp":[
                    5001,
                    8080
                  ],
                  "udp":[]
                }
              }
            }
          }
        }'
HTTP/2 201
```

> Response JSON:

```json
{
  "id":"e7ceec61-dae7-4697-aa5a-a6868fbb89ca",
  "created_at":"2019-09-17T16:03:35.397391-04:00",
  "application_id":"a1ed9f4b-0770-44d5-a5e5-c9625fe3480f",
  "network_id":"aa51a87f-f142-4341-8e94-b4b0214a009f",
  "name":"IPFS us-east-1",
  "type":"ipfs",
  "status":"init",
  "description":null,
  "config":{
    "api_port":5001,
    "container":"providenetwork-node",
    "gateway_port":8080,
    "provider_id":"docker",
    "region":"us-east-1",
    "role":"peer",
    "security":{
      "egress":"*",
      "ingress":{
        "0.0.0.0/0":{
          "tcp":[
            5001,
            8080
          ],
          "udp":null
        }
      }
    },
    "target_id":"aws"
  },
  "accessed_at":null
}
```

Create a new connector using the given configuration.


## Retrieve Connector Details

<i>Documentation forthcoming.</i>

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Connector`


## Delete Connector

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/connectors/9e5e269a-f074-49e2-8383-ab94a33ae30a
HTTP/2 204
```

Delete a configured connector.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Connector`
