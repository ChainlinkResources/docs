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
        "id": "ec81de72-c08a-432d-ac9d-664a0d021b97",
        "created_at": "2019-11-21T02:10:40.584071Z",
        "application_id": "60cad358-8d93-4d61-9f15-ecfd4a9dd9cb",
        "purpose": 44,
        "mnemonic": "twist dice country pink crystal thrive shy dumb laugh lounge liquid radar project eyebrow right monster mom hurt never whale unusual lesson squeeze seat",
        "public_key": "xpub661MyMwAqRbcGkyMb8rnET1T1KT2NMEUTNMRaiQrvR9Hnbevpt72jePhwhAxqQm1Ci4rw1XPPwcQe89Tyn6bndkNGXP8fLHdEDnL9JPMA2z",
        "private_key": "xprv9s21ZrQH143K4GttV7KmsK4iTHcXxtWd69RpnL1FN5cJuoKnHLnnBr5E6SL28ibSebnwsfdBjG7NL2UC6ZMztWcoWFRmS6UNnUGbxNh3VXV"
    },
    {
        "id": "c1e1c7fe-a038-4eb4-9f4b-ddd0de54ac36",
        "created_at": "2019-11-21T01:57:46.467658Z",
        "application_id": "60cad358-8d93-4d61-9f15-ecfd4a9dd9cb",
        "purpose": 44,
        "mnemonic": "work trip twenty sea leisure metal nerve canal demand text column like thrive wing tent equal exhibit hand canyon wolf core skill enact produce",
        "public_key": "xpub661MyMwAqRbcF9PyW5qTg8MK5Ba1hpri8wUhmLhSgkCjwyipQb2L63z6k68n4eRgwPdnU34M6ufsPMRLw7eAapx5Eu7p5HBAaEwWhN1dNiw",
        "private_key": "xprv9s21ZrQH143K2fKWQ4JTJzQaX9jXJN8rmiZ6xxHq8Qfm5BPfs3i5YFfctoCau8Q3DZHvmZDtQ1vmqEEGK2eq97Ayc1RyGTRyMKYLtmxak1X"
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
    "id": "c1e1c7fe-a038-4eb4-9f4b-ddd0de54ac36",
    "created_at": "2019-11-21T01:57:46.467658479Z",
    "application_id": "60cad358-8d93-4d61-9f15-ecfd4a9dd9cb",
    "purpose": 44,
    "mnemonic": "work trip twenty sea leisure metal nerve canal demand text column like thrive wing tent equal exhibit hand canyon wolf core skill enact produce",
    "public_key": "xpub661MyMwAqRbcF9PyW5qTg8MK5Ba1hpri8wUhmLhSgkCjwyipQb2L63z6k68n4eRgwPdnU34M6ufsPMRLw7eAapx5Eu7p5HBAaEwWhN1dNiw",
    "private_key": "xprv9s21ZrQH143K2fKWQ4JTJzQaX9jXJN8rmiZ6xxHq8Qfm5BPfs3i5YFfctoCau8Q3DZHvmZDtQ1vmqEEGK2eq97Ayc1RyGTRyMKYLtmxak1X"
}
```

Creates an HD (hierarchical deterministic) `Wallet` in accordance with BIP32. A `Wallet` may be setup as custodial or non-custodial. If the `Wallet` is custodial then the platform will derive addresses and securely persist an `Account` for each of those derived addresses.

### Request Parameters

Parameter | Description
--------- | -----------
purpose | specification to be used by the HD node subtree; set to `44` for `44'` (i.e., `0x8000002C` following the BIP43 recommendation)
