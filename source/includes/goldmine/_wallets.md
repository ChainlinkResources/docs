# Wallets

## List Wallets

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/wallets
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "efef1044-4958-43bc-903b-28f2bb938037",
        "created_at": "2018-10-03T20:48:03.24878Z",
        "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
        "user_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "address": "0xAC805F1c2Bf9a19b448bc207075B992Be29bC91a",
        "balance": null,
        "accessed_at": "2018-10-03T20:48:37.291739Z"
    }
```

This endpoint enumerates wallets used for storing cryptocurrency or tokens on behalf of Provide users managing cryptographic material (i.e., for signing transactions).

<aside class="info">Balances are returned as null here for performance reasons; see  <code>GET /api/v1/wallets/:id</code> to get balance details in the native currency for the network.</aside>


## Create Wallet

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/wallets \
     -d '{"network_id":"024ff1ef-7369-4dee-969c-1918c6edb5d4"}'
HTTP/2 201
```

> Response JSON:

```json
{
    "id": "4059f749-55ad-4c1c-975d-6c5040801079",
    "created_at": "2018-10-12T21:47:13.698524641Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "address": "0xa4f8874C971EB257C0Fd8e33401b274e2a27133d",
    "balance": null,
    "accessed_at": null
}
```

Creates a `Wallet` (also referred to as a signing identity) capable of storing cryptocurrencies and tokens native to a specific `Network`. A `Wallet` may be setup as custodial or non-custodial. If the `Wallet` is custodial then the platform will sign and broadcast transactions to the `Network` on behalf of an authorized `User` or `Application`.


## Retrieve Wallet Details

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/wallets/efef1044-4958-43bc-903b-28f2bb938037
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "efef1044-4958-43bc-903b-28f2bb938037",
    "created_at": "2018-10-03T20:48:03.24878Z",
    "application_id": "e49302c5-e485-4e14-9b0f-db5643b6a15c",
    "user_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "address": "0xAC805F1c2Bf9a19b448bc207075B992Be29bC91a",
    "balance": 0,
    "accessed_at": "2018-10-03T20:48:37.291739Z"
}
```

Retrieve details for a `Wallet`.


### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Wallet`


## Wallet Token Balance

Retrieve the on-chain token balance details for a specific `Wallet` and `Token` contract.

<i>Documentation forthcoming.</i>

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Wallet`
tokenId | id of the `Token` contract for which to retrieve the balance
