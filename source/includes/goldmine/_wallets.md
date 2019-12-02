# HD Wallets

## List HD Wallets

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/wallets
HTTP/2 200
```

> Response JSON:

```json
[
    {
        "id": "2a53547f-2e8f-4cd9-9864-e055768b779e",
        "created_at": "2019-12-02T05:31:08.455649-05:00",
        "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "purpose": 44,
        "mnemonic": "aware display shoulder circle nature glass marble hobby embody truly universe verify",
        "public_key": "xpub661MyMwAqRbcGdH28ehGpkWuGjHp4UYZZoG65FWFkzz1cqUdrn1oXR8kKWm92ESeWBATrw5tDSC7NbUUiaLsucUmBjyxgHJ9bqcNMhEiCYr",
        "private_key": "xprv9s21ZrQH143K49CZ2dAGTcaAihTKf1piCaLVGs6eCfT2k39VKEhYycpGUDAMKWHdZ9eZq6ph4G8Hsaf2haMtqEskk5Xs6DdQpgavNLRJFVK"
    },
    {
        "id": "965b33bd-1c02-4f2c-84b3-249d554d1756",
        "created_at": "2019-12-02T05:28:34.066167-05:00",
        "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "purpose": 44,
        "mnemonic": "swift exact taste divorce kitchen input avoid copy jump guitar puppy bargain",
        "public_key": "xpub661MyMwAqRbcGU19jJHtbw54SqjjWAGqFWeGbZwrMbwhvJc7VdNcYQ5BUaiAH4v9x8uhjWdxh7BXofnVsjiqoBwHoxGTZh3pqw2QmjzrCVS",
        "private_key": "xprv9s21ZrQH143K3yvgdGktEo8KtouF6hYytHifoBYEoGQj3WGxx64MzbkhdHKW1H3gHTPMCPAeExasU5wf6bcudoHaC5ZqS95gy1CmU9n8UFf"
    },
    {
        "id": "045ed108-188d-41cb-b218-967c2df6ec2a",
        "created_at": "2019-12-02T04:57:40.354586-05:00",
        "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "purpose": 44,
        "mnemonic": "same hire quit ivory yard bronze village cheap scheme laundry effort noodle",
        "public_key": "xpub661MyMwAqRbcGnt6jisuKqpRNtQ4LyhefCwCcLzmiPQqwYaUKntdPwmA7HG3NHfGM3oTJDUZZdsDvoWwnuJ1fWBgR6RHTmpDFsH1bfspe7F",
        "private_key": "xprv9s21ZrQH143K4JoddhLtxhsgprZZwWyoHz1boxbAA3ss4kFKnFaNr9SgFzziAC2vKDLMRMa2CCiZAqDq4GpWcgNX3BeSULP4mSjYDztVKoQ"
    },
    {
        "id": "7baf5ec7-0c10-40bc-80ca-93af0abc4beb",
        "created_at": "2019-12-02T04:38:48.625052-05:00",
        "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "purpose": 44,
        "mnemonic": "bird present pattern brave powder banana street fancy become gloom strong illegal",
        "public_key": "xpub661MyMwAqRbcF9SjWTQp7cG7rvtr15G8EEJanFhTm2fQjoPijpSWk9uNaWcrXvUfHhgdSq9F7cbH66EdhoMVgAE639rxWN36ZxMEeAZaKu6",
        "private_key": "xprv9s21ZrQH143K2fNGQRsokUKPJu4MbcYGs1NyysHrCh8Rs14aCH8GCMatjDKEHXzUkGB194ob5bC7R7ZzNQWd7pyso5EcvKP6oDcMG1MZude"
    },
    {
        "id": "88081786-f3d7-4907-b1af-b7f23de3a471",
        "created_at": "2019-12-02T04:24:14.846977-05:00",
        "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
        "purpose": 44,
        "mnemonic": "turn indicate cricket color agent dove garlic setup pizza slam bottom bracket",
        "public_key": "xpub661MyMwAqRbcG7pghb1JGXXjQ9fhM3BzsPZLuWhuzjn129cKR37pZBUvaNYA7a1YJ5zTsiALJVqA5mn8K6Xt8k6KyQWfSuhEH81T23EMjZx",
        "private_key": "xprv9s21ZrQH143K3dkDbZUHuPazr7qCwaU9WAdk78JJSQF29MHAsVoa1PASj6vXiVYb3QyE3eoc4oDmjAJoGG3cdGYwscCWUpRwmzxwiu6vc1D"
    }
]
```

This endpoint enumerates HD (hierarchical deterministic) wallets used for deriving addresses in accordance with BIP32.


## Create HD Wallet

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/wallets \
     -d '{"purpose": 44}'
HTTP/2 201
```

> Response JSON:

```json
{
    "id": "2a53547f-2e8f-4cd9-9864-e055768b779e",
    "created_at": "2019-12-02T05:31:08.455649-05:00",
    "application_id": "dc4152f7-456f-41ed-96b4-e52b8faa05fd",
    "path": "m/44'",
    "purpose": 44,
    "mnemonic": "aware display shoulder circle nature glass marble hobby embody truly universe verify",
    "public_key": "xpub661MyMwAqRbcGdH28ehGpkWuGjHp4UYZZoG65FWFkzz1cqUdrn1oXR8kKWm92ESeWBATrw5tDSC7NbUUiaLsucUmBjyxgHJ9bqcNMhEiCYr",
    "private_key": "xprv9s21ZrQH143K49CZ2dAGTcaAihTKf1piCaLVGs6eCfT2k39VKEhYycpGUDAMKWHdZ9eZq6ph4G8Hsaf2haMtqEskk5Xs6DdQpgavNLRJFVK"
}
```

Creates an HD (hierarchical deterministic) `Wallet` in accordance with BIP32. A `Wallet` may be setup as custodial or non-custodial. If the `Wallet` is custodial then the platform will derive addresses and securely persist an `Account` for each of those derived addresses.

### Request Parameters

Parameter | Description
--------- | -----------
purpose | specification to be used by the HD node subtree; set to `44` for `44'` (i.e., `0x8000002C` following the BIP43 recommendation)


## List Derived HD Wallet Addresses

```shell
curl -i \
     -H 'content-type: application/json' \
     -H 'authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
     https://goldmine.provide.services/api/v1/wallets/88081786-f3d7-4907-b1af-b7f23de3a471/accounts?page=1
HTTP/2 200
```

> Response JSON:

```json
[
    {
        "address": "0xCCC071f01dB7D2541A73dF05FfE568e7F937ADE9",
        "hd_derivation_path": "m/44'/60'/0'/0/0",
        "private_key": "98e0908da8800ca0b0b5c4005d82fb20de06efc670d9a0fab7113b2ea9d61532",
        "public_key": "2f2ddb3d536d7e8e7d387235ff389e92e3367890444e47051e32bdfe0fdb13dd1744b1fa9164990fac5b895d833b055bd58dc85ec2d31f6a3d502098e69ada75"
    },
    {
        "address": "0x15C67CDA4c10E83f08adfD731480B12C1D48B66D",
        "hd_derivation_path": "m/44'/60'/0'/0/1",
        "private_key": "5ee17f3182fa12ab700d15b89d60c54091cc98503d2c62d6a273e2efe8bc42ed",
        "public_key": "51e4513473444438e1a5c02139dcd87a813760371716661306bd7a8f2e815d526ca5292fb2b1edeeaf871e94807698e2f1703d4af8a18bf4989985407533d0ef"
    },
    {
        "address": "0x14fD7e79097C0879ccA2EEA2a6C950E1DFC42FA4",
        "hd_derivation_path": "m/44'/60'/0'/0/2",
        "private_key": "46d96b99f0ec13431580ab794cd0beca1d38c0cd107754c0a0c69688896b0369",
        "public_key": "bac44b1e1ec08400be0772a030bbc25968ae0622f365fa181d6a155f5f13dbbf012f3e3ce8ee59a748fc385cd91a1d9b6643c12a8993f4bd92292f20b84d46f6"
    },
    {
        "address": "0xE83Ea09F2A3439e677679A068bca389a35b2f52D",
        "hd_derivation_path": "m/44'/60'/0'/0/3",
        "private_key": "f2d65405004213bc899ca083aed33844a487074ae9ac39ac9e708c08f37be2b1",
        "public_key": "8879c1d805c063978f26144b9b85921f63fe26ba3f5f58adb9e97221924b7070341396ac79ff416e0d82f9806119f6cfb87b9c30505d84c190cbd7979576111b"
    },
    {
        "address": "0xA5cfcF1c0B0b4a2EDC8352Ad1e4aF5A74CAA00Ee",
        "hd_derivation_path": "m/44'/60'/0'/0/4",
        "private_key": "847951b56e931598d631ddbe3a0b56465387675c48a7cbfaf62f95bb2d2fd185",
        "public_key": "3aca22d5de6ddb53f8bbbad31c7b85a52457b472efe72e017c227b3e8cb760662f6e739a365f978f06a200d18a4fb083123dd371374f483f8c567af21117e557"
    },
    {
        "address": "0xB02C049CC158c672260a94E9a9E37A6509d7C6FF",
        "hd_derivation_path": "m/44'/60'/0'/0/5",
        "private_key": "1e6269992637a778b43dc053ff262371990acce2807ba1f0260398d6629d2800",
        "public_key": "ff72e60771481e8592d550504bc45051a55ce9ddaf1078c9bfe620b26ae76346a800140e2f700f85920beb545104ac16f15c65805a156684a1f5d0dc558ceea8"
    },
    {
        "address": "0x223b4FC2B63B2Ff1069Ad3A9d434335B25d16D19",
        "hd_derivation_path": "m/44'/60'/0'/0/6",
        "private_key": "15ea4554e890c74385c35bb61e2446b3ffb8068c2c789a70e93089a5dea8b7dc",
        "public_key": "4a930c1313b7ed3af8c012214baf148e9a06931bbc7296bbc131fa8888d90c3c4859ee1a1586295f805baa349def98b6ee2b4c07cfcad23ab6f6e5273e20f809"
    },
    {
        "address": "0xA940168B748c8361e7374f8b1AC3e8f336DEc2aC",
        "hd_derivation_path": "m/44'/60'/0'/0/7",
        "private_key": "a1c7f2c6f8543a34decdf4cf1c51ce3167bdf8e709bed8dfbe64d839751b363c",
        "public_key": "028384b15be0e9691a0f340de85027438aa579d8a072e76f5fb69d01a0dbd36ba5de07da9431d2386f135f89add99cc6afbd9998f9d87443b0e8f3810a0a0ab5"
    },
    {
        "address": "0x58cA9a0Cb435b28c49a9EBeaFD78Aa9fdB60C127",
        "hd_derivation_path": "m/44'/60'/0'/0/8",
        "private_key": "5ee907d6502174ab860201dd6814e9bcb1a711e608efb49659a5370bbef6bc6d",
        "public_key": "0ec3e23857d0471a62239f72b7fbf15563cfde6b3e9adfeea096375e9e95ce13c6e3702850a71e3fe39e812eacb7c7bc460e4489e1f5c480395f16a708f138c6"
    },
    {
        "address": "0x06edC8270467cfca263F0Dfd44Ae835Fef2a3bF7",
        "hd_derivation_path": "m/44'/60'/0'/0/9",
        "private_key": "6a001a5035f428582df433a3db3c06f6717dd03c44580bf04a5b867dbc83f7e8",
        "public_key": "b1c1407c89c133f8ffc3de1e6bdf9f0fcb3f8e9fb506ce113a95a7ef2f16a0adb6dd60413470f2a8284f512c53dff346c432796835d29087308d413219a37583"
    }
]
```

This endpoint returns a paginated list of the derived addresses for a specific derivation path for a specific HD (hierarchical deterministic) wallet.

The HD derivation path for each derived address is returned. The returned addresses are not currently being "pinned" (or otherwise persisted) by the API; as such, an ephemeral representation of the `Account`, complete with its derived key material, is returned by the API.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the HD `Wallet`

### Query Parameters

Parameter | Description
--------- | -----------
coin_type | the coin type, per BIP44
index | the index of the account or identity, per BIP44
chain_path | a constant representing the internal or external chain path, per BIP44; public derivation is used at this level

In addition to the above parameters, `page` and `rpp` pagination query parameters are supported.
