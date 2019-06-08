# Network Nodes

## List Network Nodes

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "59d1e7ce-3316-45b2-bf06-5fae2c6294fe",
    "created_at": "2018-09-06T08:13:14.109926Z",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
    "is_bootnode": true,
    "host": "ec2-18-206-200-4.compute-1.amazonaws.com",
    "description": null,
    "role": "peer",
    "status": "running",
    "config": {
      "default_json_rpc_port": null,
      "default_websocket_port": null,
      "engine_id": "authorityRound",
      "env": {
        "BOOTNODES": "enode://eb0543bf6c960ad79...",
        "CHAIN": "unicorn-v0",
        "CHAIN_SPEC_URL": "https://console.provide.services:443/api/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/spec.json?x-api-authorization=MjE3Nzc4...",
        "ENGINE_SIGNER": "0xc8cf82765ccc99e5d878A245f7eC9ECe8F9Fae4d",
        "ENGINE_SIGNER_KEY_JSON": "{\"id\":\"120354c2-f2d5-...\"}",
        "ENGINE_SIGNER_PRIVATE_KEY": "b9dc0beec2d7f9...",
        "NETWORK_ID": "22",
        "PEER_SET": "required:eb0543bf6c960ad79a9..."
      },
      "peer_url": "enode://46cd112cbcc91cfe410a697...",
      "protocol_id": "poa",
      "provider_id": "docker",
      "region": "us-east-1",
      "role": "peer",
      "target_id": "aws",
      "target_security_group_ids": [
        "sg-0f29ec025b64c0a44"
      ],
      "target_task_ids": [
        "arn:aws:ecs:us-east-1:085843810865:task/58953fe..."
      ]
    }
  }
```

This endpoint enumerates the specified Network’s Nodes.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`


## Deploy Network Node

```shell
curl -i \
    -H 'Authorization: bearer youR-ToKEn' \
    https://goldmine.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/nodes \
    -d '{
  "network_id": "4617eb8c-4f74-4262-b626-9616ab6fa413",
  "config": {
    "protocol_id": "poa",
    "engine_id": "authorityRound",
    "target_id": "aws",
    "provider_id": "docker",
    "role": "validator",
    "engines": "[{\"id\":\"authorityRound\",\"name\":\"Authority Round\",\"enabled\":true}]",
    "providers": "[{\"id\":\"ubuntu-vm\",\"name\":\"Ubuntu\",\"...\":\"...\"}]",
    "roles": "[{\"id\":\"peer\",\"name\":\"Peer\",\"config\":{\"...\":\"...\"]}]",
    "credentials": {
      "aws_access_key_id": "AKIA...",
      "aws_secret_access_key": "MtM/6RZw0..."
    },
    "env": {
      "CHAIN_SPEC_URL": "https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGci...",
      "CHAIN": "unicorn-v0",
      "ENGINE_SIGNER": "0x...",
      "NETWORK_ID": "1539570139"
    },
    "rc.d": "{\n  \"CHAIN_SPEC_URL\": \"https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGciOiJI...\",\n  \"CHAIN\": \"unicorn-v0\",\n  \"ENGINE_SIGNER\": \"0x...\",\n  \"NETWORK_ID\": \"1539570139\",\n  \"ENGINE_SIGNER_PRIVATE_KEY\": null\n}",
    "region": "us-east-1"
  }
}'
```

> Response JSON:

```json
{
  "id": "4721cca3-fa2e-4085-b675-c5bea777c408",
  "created_at": "2018-10-15T02:42:10.375957413Z",
  "network_id": "4617eb8c-4f74-4262-b626-9616ab6fa413",
  "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
  "is_bootnode": false,
  "host": null,
  "description": null,
  "role": "validator",
  "status": "pending",
  "config": {
    "protocol_id": "poa",
    "engine_id": "authorityRound",
    "target_id": "aws",
    "provider_id": "docker",
    "role": "validator",
    "engines": "[{\"id\":\"authorityRound\",\"name\":\"Authority Round\",\"enabled\":true}]",
    "providers": "[{\"id\":\"ubuntu-vm\",\"name\":\"Ubuntu\",\"img_src_dark\":\"...\"}]",
    "roles": "[{\"id\":\"peer\",\"name\":\"Peer\",\"config\":{...}]",
    "credentials": {
      "aws_access_key_id": "AKIAJ5Y...",
      "aws_secret_access_key": "MtM/6..."
    },
    "env": {
      "CHAIN_SPEC_URL": "https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGciOiJIUz...",
      "CHAIN": "unicorn-v0",
      "ENGINE_SIGNER": "0x16E8950...",
      "NETWORK_ID": "1539570139"
    },
    "rc.d": "{\n  \"CHAIN_SPEC_URL\": \"https://api.provide.services/api/networks/4617eb8c-4f74-4262-b626-9616ab6fa413/spec.json?x-api-authorization=eyJhbGci...\",\n  \"CHAIN\": \"unicorn-v0\",\n  \"ENGINE_SIGNER\": \"0x...\",\n  \"NETWORK_ID\": \"1539570139\",\n  \"ENGINE_SIGNER_PRIVATE_KEY\": null\n}",
    "region": "us-east-1"
  }
}
```

Configure a `NetworkNode` to join a specific peer-to-peer `Network`. Upon successful validation and creation of the `NetworkNode` the platform attempts to deploy it asynchronously. Depending on the `Network` (i.e., its consensus protocol, security model, etc.) and the target infrastructure (i.e., AWS, Azure or locally via Docker), various enrichment of the deployed `NetworkNode` occurs. See [Orchestration](#orchestration).

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`


## Retrieve Network Node Details

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "59d1e7ce-3316-45b2-bf06-5fae2c6294fe",
    "created_at": "2018-09-06T08:13:14.109926Z",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
    "is_bootnode": true,
    "host": "ec2-18-206-200-4.compute-1.amazonaws.com",
    "description": null,
    "role": "peer",
    "status": "running",
    "config": {
        "credentials": {
            "aws_access_key_id": "AKIAIF...",
            "aws_secret_access_key": "azrrYySnS..."
        },
        "default_json_rpc_port": null,
        "default_websocket_port": null,
        "engine_id": "authorityRound",
        "engines": [
            {
                "enabled": true,
                "id": "authorityRound",
                "name": "Authority Round"
            }
        ],
        "env": {
            "BOOTNODES": "enode://eb0543bf6c9...",
            "CHAIN": "unicorn-v0",
            "CHAIN_SPEC_URL": "https://console.provide.services:443/api/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/spec.json?x-api-authorization=MjE3N...",
            "ENGINE_SIGNER": "0xc8...",
            "ENGINE_SIGNER_KEY_JSON": "{\"id\":\"...\"}",
            "ENGINE_SIGNER_PRIVATE_KEY": "b9dc0...",
            "NETWORK_ID": "22",
            "PEER_SET": "required:eb0543bf6c960a..."
        },
        "peer_url": "enode://46cd112cbcc91cfe410...",
        "protocol_id": "poa",
        "provider_id": "docker",
        "providers": [
            {
                "enabled": true,
                "id": "ubuntu-vm",
                "img_src": "https://s3.amazonaws.com/provide.services/img/ubuntu.png",
                "name": "Ubuntu"
            },
            {
                "enabled": true,
                "id": "docker",
                "img_src": "https://s3.amazonaws.com/provide.services/img/docker.png",
                "name": "Docker"
            }
        ],
        "rc.d": "{\n  \"CHAIN_SPEC_URL\": \"https://console.provide.services:443/api/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/spec.json?x-api-authorization=MjE3Nzc...\",\n  \"BOOTNODES\": \"enode://eb0543bf6c9...\",\n  \"NETWORK_ID\": \"22\"\n}",
        "region": "us-east-1",
        "role": "peer",
        "roles": [
            {
                "config": {
                    "allows_multiple_deployment": true,
                    "default_rcd": {
                        "provide.network": "#!/bin/bash\n\nservice provide.network stop\n...\n"
                    },
                    "quickclone_recommended_node_count": 2
                },
                "id": "peer",
                "name": "Peer",
                "supported_provider_ids": [
                    "ubuntu-vm",
                    "docker"
                ]
            },
            {
                "config": {
                    "allows_multiple_deployment": false,
                    "default_rcd": {
                        "docker": {
                            "provide.network": "{\"CHAIN_SPEC_URL\": null, \"ENGINE_SIGNER\": null, \"NETWORK_ID\": null, \"ENGINE_SIGNER_PRIVATE_KEY\": null}"
                        },
                        "ubuntu-vm": {
                            "provide.network": "#!/bin/bash\n\nservice provide.network stop\n...\n"
                        }
                    },
                    "quickclone_recommended_node_count": 1
                },
                "id": "validator",
                "name": "Validator",
                "supported_provider_ids": [
                    "ubuntu-vm",
                    "docker"
                ]
            },
            {
                "config": {
                    "allows_multiple_deployment": false,
                    "default_rcd": {
                        "docker": {
                            "provide.network": "{\"JSON_RPC_URL\": null}"
                        }
                    },
                    "quickclone_recommended_node_count": 1
                },
                "id": "explorer",
                "name": "Block Explorer",
                "supported_provider_ids": [
                    "ubuntu-vm",
                    "docker"
                ]
            }
        ],
        "target_id": "aws",
        "target_security_group_ids": [
            "sg-0f29..."
        ],
        "target_task_ids": [
            "arn:aws:ecs:us-east-1:085843810865:task/58953..."
        ]
    }
}
```

This endpoint retrieves the details of the Network’s specified Node.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | id of the `NetworkNode`


## Retreive Network Node Logs

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe/logs
HTTP/2 200
```

> The above command returns logs structured like this:

```[
    "2018-10-12 03:07:50 UTC Verifier #1 INFO import  Imported #2532534 0x4720…9c60 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:07:53 UTC IO Worker #1 INFO import          #0    3/25 peers      5 MiB chain   95 MiB db  0 bytes queue  573 KiB sync  RPC:  0 conn,    0 req/s,  179 µs",
    "2018-10-12 03:07:55 UTC Verifier #0 INFO import  Imported #2532535 0xb01b…3150 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:00 UTC Verifier #1 INFO import  Imported #2532536 0x64c7…b825 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:05 UTC Verifier #0 INFO import  Imported #2532537 0xccb4…d9da (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:10 UTC Verifier #1 INFO import  Imported #2532538 0x70ed…97ea (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:15 UTC Verifier #0 INFO import  Imported #2532539 0x75c5…1712 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:20 UTC Verifier #1 INFO import  Imported #2532540 0xbb17…a470 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:25 UTC Verifier #0 INFO import  Imported #2532541 0x61d8…37a8 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 03:08:28 UTC IO Worker #2 INFO import          #0    3/25 peers      5 MiB chain   95 MiB db  0 bytes queue  573 KiB sync  RPC:  0 conn,    0 req/s,  167 µs",
    ...
    "2018-10-12 11:42:30 UTC Verifier #0 INFO import  Imported #2538710 0x320b…da62 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:35 UTC Verifier #1 INFO import  Imported #2538711 0x00b2…3346 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:40 UTC Verifier #0 INFO import  Imported #2538712 0xdbba…9811 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:45 UTC Verifier #1 INFO import  Imported #2538713 0x473d…2c6c (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:50 UTC Verifier #0 INFO import  Imported #2538714 0x194a…fffb (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:42:55 UTC Verifier #1 INFO import  Imported #2538715 0xd854…cca5 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:43:00 UTC Verifier #0 INFO import  Imported #2538716 0x5249…1343 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:43:04 UTC IO Worker #1 INFO import          #0    3/25 peers      4 MiB chain   95 MiB db  0 bytes queue  573 KiB sync  RPC:  0 conn, 6558 req/s,  173 µs",
    "2018-10-12 11:43:05 UTC Verifier #1 INFO import  Imported #2538717 0xdf84…3b4d (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)",
    "2018-10-12 11:43:10 UTC Verifier #1 INFO import  Imported #2538718 0x888d…7b65 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
]
```

This endpoint retrieves paginated logs for a network node.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | the id of the `NetworkNode`


## Undeploy Network Node

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe
HTTP/2 204
```

Undeploy a `NetworkNode`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | the id of the `NetworkNode`
