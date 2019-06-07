# Transactions

## List Transactions


```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/transactions
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "fb4c5912-628f-4d8e-9c67-76d379010a71",
        "created_at": "2018-10-03T20:48:37.292823Z",
        "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
        "user_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
        "to": null,
        "value": 0,
        "data": "0x608060405234801561001057600080fd5b50610704806100206000396000f300608060405260...",
        "hash": "0xf769d96671abfd8c7dfe9b747db1380d1b974d6282833e573900bad7b11e51e5",
        "status": "success",
        "params": null,
        "traces": null,
        "ref": null,
        "description": null
    }
```

This endpoint enumerates transactions.





## Post a Transaction using a Wallet

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/transactions \
     -d '{"network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4", "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037", "to": "0xfb17cB7bb99128AAb60B1DD103271d99C8237c0d", "value": 0}'
HTTP/2 201
```

> Response JSON:

```json
{
    "id": "6759791c-71b5-4fb1-bf19-5488a9f9ee1e",
    "created_at": "2018-10-15T04:04:47.903585906Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
    "to": "0xfb17cB7bb99128AAb60B1DD103271d99C8237c0d",
    "value": 0,
    "data": null,
    "hash": "0xbc2a0fb68c06d5c2fa603fb7131c3922c4b3b19ece56ee8f8a7d241a9064233e",
    "status": "pending",
    "params": null,
    "traces": null,
    "ref": null,
    "description": null
}
```
> If the broadcast transaction represents a contract deployment, a contract will be created implicitly after deployment is confirmed with the Network. The following example represents a Contract creation with provided params specific to the Ethereum network.

```shell
curl -i \
    -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/transactions \
    -d '{
  "network_id": "ba02ff92-f5bb-4d44-9187-7e1cc214b9fc",
  "wallet_id": "ce1fa3b8-049e-467b-90d8-53b9a5098b7b",
  "data": "60606040526003805460a060020a60ff021916905560006...",
  "params": {"name": "ProvideToken",
                "abi": [
                  {
                    "constant": true,
                    "inputs": [
                      {
                        "name": "_holder",
                        "type": "address"
                      }
                    ],
                    "name": "tokenGrantsCount",
                    "outputs": [
                      {
                        "name": "index",
                        "type": "uint256"
                      }
                    ],
                    "payable": false,
                    "type": "function"
                  },
                  ...
                  {
                    "anonymous": false,
                    "inputs": [
                      {
                        "indexed": true,
                        "name": "from",
                        "type": "address"
                      },
                      {
                        "indexed": true,
                        "name": "to",
                        "type": "address"
                      },
                      {
                        "indexed": false,
                        "name": "value",
                        "type": "uint256"
                      }
                    ],
                    "name": "Transfer",
                    "type": "event"
                  }
                ]
              }
            }'
HTTP/2 422
```
> Response JSON:

```json
{
    "id": "6759791c-71b5-4fb1-bf19-5488a9f9ee1e",
    "created_at": "2018-10-15T04:04:47.903585906Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
    "to": "0xfb17cB7bb99128AAb60B1DD103271d99C8237c0d",
    "value": 0,
    "data": null,
    "hash": "0xbc2a0fb68c06d5c2fa603fb7131c3922c4b3b19ece56ee8f8a7d241a9064233e",
    "status": "pending",
    "params": null,
    "traces": null,
    "ref": null,
    "description": null
}
```


This endpoint prepares and signs a protocol Transaction using a Wallet on behalf of a specific application User and broadcasts the transaction to the public blockchain Network.

Under certain conditions, calling this API will result in a transaction being created which requires lifecycle management (i.e., in the case when a managed Sidechain has been configured to scale micropayment channels and/or coalesce an application’s transactions for on-chain settlement).





## Retrieve a Transaction

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/transactions/fb4c5912-628f-4d8e-9c67-76d379010a71
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "fb4c5912-628f-4d8e-9c67-76d379010a71",
    "created_at": "2018-10-03T20:48:37.292823Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "efef1044-4958-43bc-903b-28f2bb938037",
    "to": null,
    "value": 0,
    "data": "0x608060405234801561001057600080fd5b506...",
    "hash": "0xf769d96671abfd8c7dfe9b747db1380d1b97...",
    "status": "success",
    "params": null,
    "traces": {
        "result": [
            {
                "action": {
                    "callType": null,
                    "from": "0xac805f1c2bf9a19b448bc207075b992be29bc91a",
                    "gas": "0x57caf",
                    "init": "0x608060405234801561001057600080f...",
                    "input": null,
                    "to": null,
                    "value": "0x0"
                },
                "blockHash": "0x4a5e8e1bf594dc4df5c54c4b9c91f...",
                "blockNumber": 2389804,
                "result": {
                    "address": "0x2a3d64307a551a1f2902867f5b2437bc52f0c5c4",
                    "code": "0x6080604052600436106100565763ffffffff7c010000000...",
                    "gasUsed": "0x57caf",
                    "output": null
                },
                "error": null,
                "subtraces": 0,
                "traceAddress": [],
                "transactionHash": "0xf769d96671abfd8c7dfe9b747db138...",
                "transactionPosition": 0,
                "type": "create"
            }
        ]
    },
    "ref": null,
    "description": null
}
```

This endpoint retrieves details for a specific Transaction.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the Transaction
