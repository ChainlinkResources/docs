# Smart Contracts

## List Contracts

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/contracts
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "7ede6b96-874a-424d-ae85-669c1c90dfb8",
        "created_at": "0001-01-01T00:00:00Z",
        "application_id": null,
        "network_id": "4e9e29de-fbd2-4d6a-962e-93bc55c1a306",
        "contract_id": null,
        "transaction_id": null,
        "name": "Network Contract 0x0000000000000000000000000000000000000009",
        "address": "0x0000000000000000000000000000000000000009",
        "params": null,
        "accessed_at": null
    },
    ...
    {
        "id": "652befe6-6cc7-42b2-8994-eeaa98adbf0e",
        "created_at": "0001-01-01T00:00:00Z",
        "application_id": null,
        "network_id": "73c82453-2a19-4f2a-86c6-37f66ae78189",
        "contract_id": null,
        "transaction_id": null,
        "name": "Network Contract 0x0000000000000000000000000000000000000009",
        "address": "0x0000000000000000000000000000000000000009",
        "params": null,
        "accessed_at": null
    }
```

This endpoint enumerates managed smart contracts.




### Query Parameters

Parameter | Default | Description
--------- | ----- | -----------
filter_tokens | true | Filters token contracts from the response

## Deploy a Contract

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/contracts \
    -d '{"network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
          "wallet_id": "86ee6d48-66bb-4122-8073-a078854d09e6",
          "data": "0x608060405234...",
          "params": {
            "name": "X12",
            "abi": [
              {
                "constant": false,
                "inputs": [
                  {
                    "name": "sndr_interchange_id",
                    "type": "string"
                  }
                ],
                "name": "send",
                "outputs": [
                ],
                "payable": false,
                "stateMutability": "nonpayable",
                "type": "function"
              }
            ]
          },
          "lang": "bytecode",
          "id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d"
        }'
HTTP/2 201
```

> Response JSON:

```json
{
  "id": "fccd7404-2eef-4545-a302-5027f60b46d5",
  "created_at": "2018-10-15T03:46:50.138510202Z",
  "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
  "user_id": null,
  "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
  "wallet_id": "86ee6d48-66bb-4122-8073-a078854d09e6",
  "to": null,
  "value": 0,
  "data": "0x6080604052...",
  "hash": "0x2bdd0f991...",
  "status": "pending",
  "params": {
    "name": "X12",
    "abi": [
      {
        "constant": false,
        "inputs": [
          {
            "name": "sndr_interchange_id",
            "type": "string"
          },
          ...
          {
            "name": "edi_payload",
            "type": "string"
          }
        ],
        "name": "send",
        "outputs": null,
        "payable": false,
        "stateMutability": "nonpayable",
        "type": "function"
      },
        "name": "makeOffer",
        "outputs": null,
        "payable": false,
        "stateMutability": "nonpayable",
        "type": "function"
      }
    ]
  },
  "traces": null,
  "ref": null,
  "description": null
}
```

This endpoint deploys a new contract.





## Get a Specific Contract

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/contracts/55271393-34c7-4d53-8aa8-4a4b06554c1a
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "55271393-34c7-4d53-8aa8-4a4b06554c1a",
    "created_at": "2018-09-21T14:23:19.926668Z",
    "application_id": "25b6339c-f11f-4a00-94d7-0a6e9b64586d",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "contract_id": null,
    "transaction_id": "4bca28a4-7c11-44c0-aba3-acc360421a05",
    "name": "X12",
    "address": "0x61D0deE3E758d73D411c04364bCD56606b1fB833",
    "params": {
        "abi": [
            {
                "constant": false,
                "inputs": [
                    {
                        "name": "sndr_interchange_id",
                        "type": "string"
                    },
                    ...
                    {
                        "name": "edi_payload",
                        "type": "string"
                    }
                ],
                "name": "send",
                "outputs": null,
                "payable": false,
                "stateMutability": "nonpayable",
                "type": "function"
            },
            {
                "constant": true,
                "inputs": null,
                "name": "ipfs_fields",
                "outputs": [
                    {
                        "name": "",
                        "type": "bytes32[]"
                    }
                ],
                "payable": false,
                "stateMutability": "pure",
                "type": "function"
            },
            {
                "constant": true,
                "inputs": null,
                "name": "fave_field",
                "outputs": [
                    {
                        "name": "",
                        "type": "bytes32"
                    }
                ],
                "payable": false,
                "stateMutability": "pure",
                "type": "function"
            }
        ],
        "name": "X12"
    },
    "accessed_at": "2018-10-13T05:29:58.539991Z"
}
```

This endpoint retrieves details for the specified Contract.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the contract

## Execute a Specific Contract

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/contracts/3b9fe62e-5da7-43dc-838f-3cfa1421ed0f/execute \
     -d '{"wallet_id": "a-signing-identity-identifier", "method": "a_method_from_the_contract", "params": ["arguments", "for", "the", "method"], "value": 0.5}'
HTTP/2 202
```

> Response JSON:

```json
{
    "ref": "specifics-depend-on-the-nature-of-the-contract-and-method"
}
```

This endpoint executes specific functionality encapsulated within a given Contract.




### Request Body details

- `wallet_id` is the signing identity to use for the request
- `method` is the function name from the contract to invoke
- `params` is an array of values to pass as arguments to the method
- `value` is the amount of token transfer

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the contract
