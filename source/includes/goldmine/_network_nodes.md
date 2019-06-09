# Network Nodes

## List Network Nodes

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/ef976635-545b-46c6-9576-4e3a893a68e9/nodes
HTTP/2 200
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
content-type: application/json; charset=UTF-8
date: Sun, 09 Jun 2019 08:18:10 GMT
content-length: 2026
x-total-results-count: 1
```

> Response JSON:

```json
[
    {
        "id": "db51383c-92cd-4f0a-8ce7-881b70c420ea",
        "created_at": "2019-06-09T05:04:23.378247-04:00",
        "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
        "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
        "application_id": null,
        "is_bootnode": true,
        "host": null,
        "ipv4": null,
        "ipv6": null,
        "private_ipv4": null,
        "private_ipv6": null,
        "description": null,
        "role": "validator",
        "status": "genesis",
        "config": {
            "default_json_rpc_port": null,
            "default_websocket_port": null,
            "engine_id": "authorityRound",
            "env": {
                "CHAIN": "dawn",
                "CHAIN_SPEC_URL": "https://www.dropbox.com/s/xbuadz3odhpux7i/spec-us-east-2.json?dl=1",
                "CLIENT": "parity",
                "ENGINE_SIGNER": "0x549871a39Eeb7E406C1E4b199A8A46962fB78a9C",
                "FAT_DB": "on",
                "NETWORK_ID": "1560058202",
                "PRUNING": "archive",
                "TRACING": "on"
            },
            "protocol_id": "poa",
            "provider_id": "docker",
            "region": "us-east-2",
            "role": "validator",
            "security": {
                "egress": "*",
                "ingress": {
                    "0.0.0.0/0": {
                        "tcp": [
                            5001,
                            8050,
                            8051,
                            8080,
                            30300
                        ],
                        "udp": [
                            30300
                        ]
                    }
                }
            },
            "target_id": "aws",
            "target_security_group_ids": [
                "sg-0decccab90d31da82"
            ],
            "target_task_ids": [
                "arn:aws:ecs:us-east-2:085843810865:task/d7529823-332e-4004-98c3-d89058653734"
            ]
        }
    }
]
```

List `NetworkNodes` for a `Network`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`


## Deploy Network Node

```shell
curl -i -XPOST \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NjAwNTg0NTksImp0aSI6IjU0YWZmMGQ1LTFjY2ItNDRmNy1iYTRiLTExYTA3YWFhZGM2YiIsInN1YiI6InVzZXI6NTE4MzE5MmQtYWM4NS00YzVhLWE3OGQtODAzMWE4ZDIwODc4In0.jI7S0gW__iFjbZi0o8AKyqrH8D01vpCpgV3HOh9TrUE' \
    -H 'Content-Type: application/json' \
    https://goldmine.provide.services/api/networks/ef976635-545b-46c6-9576-4e3a893a68e9/nodes \
    -d '{
    "config":{
        "credentials":{
            "aws_access_key_id":"AKIXXXXXXXXXXXXXXXXX",
            "aws_secret_access_key":"75yXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
        },
        "engine_id":"authorityRound",
        "env":{
            "CHAIN_SPEC_URL":"https://www.dropbox.com/s/xbuadz3odhpux7i/spec-us-east-2.json?dl=1",
            "ENGINE_SIGNER":"0x549871a39Eeb7E406C1E4b199A8A46962fB78a9C",
            "NETWORK_ID":"1560058202",
            "FAT_DB":"on",
            "PRUNING":"archive",
            "TRACING":"on"
        },
        "protocol_id":"poa",
        "provider_id":"docker",
        "region":"us-east-2",
        "role":"validator",
        "target_id":"aws"
    }
}'
```

> Response JSON:

```json
{
    "id": "eb81ab38-4dc6-45c6-8c4d-5d5645fd3079",
    "created_at": "2019-06-09T03:53:50.505646-04:00",
    "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
    "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
    "application_id": null,
    "is_bootnode": false,
    "host": null,
    "ipv4": null,
    "ipv6": null,
    "private_ipv4": null,
    "private_ipv6": null,
    "description": null,
    "role": "validator",
    "status": "pending",
    "config": {
        "engine_id": "authorityRound",
        "env": {
            "CHAIN_SPEC_URL": "https://www.dropbox.com/s/xbuadz3odhpux7i/spec-us-east-2.json?dl=1",
            "ENGINE_SIGNER": "0x549871a39Eeb7E406C1E4b199A8A46962fB78a9C",
            "FAT_DB": "on",
            "NETWORK_ID": "1560058202",
            "PRUNING": "archive",
            "TRACING": "on"
        },
        "protocol_id": "poa",
        "provider_id": "docker",
        "region": "us-east-2",
        "role": "validator",
        "target_id": "aws"
    }
}
```

Configure a `NetworkNode` to join a specific peer-to-peer `Network`. Upon successful validation and creation of the `NetworkNode` the platform attempts to deploy it asynchronously. Depending on the `Network` (i.e., its consensus protocol, security model, etc.) and the target infrastructure (i.e., AWS, Azure or locally via Docker), various enrichment of the deployed `NetworkNode` occurs. See [Orchestration](#orchestration).

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`

### Request Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`


## Retrieve Network Node Details

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/ef976635-545b-46c6-9576-4e3a893a68e9/nodes/eb81ab38-4dc6-45c6-8c4d-5d5645fd3079
HTTP/2 200
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
content-type: application/json; charset=UTF-8
date: Sun, 09 Jun 2019 08:18:10 GMT
content-length: 1000
```

> Response JSON:

```json
{
    "id": "eb81ab38-4dc6-45c6-8c4d-5d5645fd3079",
    "created_at": "2019-06-09T03:53:50.505646-04:00",
    "network_id": "ef976635-545b-46c6-9576-4e3a893a68e9",
    "user_id": "5183192d-ac85-4c5a-a78d-8031a8d20878",
    "application_id": null,
    "is_bootnode": true,
    "host": "ec2-3-16-28-39.us-east-2.compute.amazonaws.com",
    "ipv4": "3.16.28.39",
    "ipv6": null,
    "private_ipv4": "172.31.19.91",
    "private_ipv6": null,
    "description": null,
    "role": "validator",
    "status": "running",
    "config": {
        "default_json_rpc_port": null,
        "default_websocket_port": null,
        "engine_id": "authorityRound",
        "env": {
            "CHAIN": "dawn",
            "CHAIN_SPEC_URL": "https://www.dropbox.com/s/xbuadz3odhpux7i/spec-us-east-2.json?dl=1",
            "CLIENT": "parity",
            "ENGINE_SIGNER": "0x549871a39Eeb7E406C1E4b199A8A46962fB78a9C",
            "FAT_DB": "on",
            "NETWORK_ID": "1560058202",
            "PRUNING": "archive",
            "TRACING": "on"
        },
        "peer_url": "enode://9d83bd776c6cea1f961037ebdd0150b5ba04053038379b3c46293188052e7b98046675f6efaaea6f6851e6c5b651b9d7dd89b734564877744f3b87338090f4ca@172.31.19.91:30300",
        "protocol_id": "poa",
        "provider_id": "docker",
        "region": "us-east-2",
        "role": "validator",
        "security": {
            "egress": "*",
            "ingress": {
                "0.0.0.0/0": {
                    "tcp": [
                        5001,
                        8050,
                        8051,
                        8080,
                        30300
                    ],
                    "udp": [
                        30300
                    ]
                }
            }
        },
        "target_id": "aws",
        "target_security_group_ids": [
            "sg-0d1af5799e7669858"
        ],
        "target_task_ids": [
            "arn:aws:ecs:us-east-2:085843810865:task/7ca2bc60-0fd0-4403-b693-bf232d5c0239"
        ]
    }
}
```

Retrieve details for a `NetworkNode`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | id of the `NetworkNode`


## Retreive Network Node Logs

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/ef976635-545b-46c6-9576-4e3a893a68e9/nodes/eb81ab38-4dc6-45c6-8c4d-5d5645fd3079/logs
HTTP/2 200
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
content-type: application/json; charset=UTF-8
date: Sun, 09 Jun 2019 08:12:47 GMT
```

> Response JSON:

```json
[
    "Starting client: parity",
    "IPFS daemon starting; bin: /usr/local/bin/ipfs",
    "Initializing daemon...",
    "Swarm listening on /ip4/127.0.0.1/tcp/4001",
    "Swarm listening on /ip4/169.254.172.42/tcp/4001",
    "Swarm listening on /ip4/172.31.19.91/tcp/4001",
    "Swarm listening on /p2p-circuit/ipfs/QmYv5vmq3Fa24AgQG9tik7cP6pxdBk5koVYqHGuB3XWKwM",
    "Swarm announcing /ip4/127.0.0.1/tcp/4001",
    "Swarm announcing /ip4/169.254.172.42/tcp/4001",
    "Swarm announcing /ip4/172.31.19.91/tcp/4001",
    "API server listening on /ip4/0.0.0.0/tcp/5001",
    "Gateway (readonly) server listening on /ip4/0.0.0.0/tcp/8080",
    "Daemon is ready",
    "Found invalid characters in bootnodes.txt",
    "provide.network node starting in /opt; parity bin: /usr/bin/parity",
    "2019-06-09 07:58:41 UTC main INFO parity_ethereum::run  Starting Parity-Ethereum/v2.5.0-beta-b52ac20-20190408/x86_64-linux-gnu/rustc1.33.0",
    "2019-06-09 07:58:41 UTC main INFO parity_ethereum::run  Keys path /opt/keys/dawn",
    "2019-06-09 07:58:41 UTC main INFO parity_ethereum::run  DB path /opt/chains/dawn/db/6df54e29399e56eb",
    "2019-06-09 07:58:41 UTC main INFO parity_ethereum::run  State DB configuration: archive +Fat +Trace",
    "2019-06-09 07:58:41 UTC main INFO parity_ethereum::run  Operating mode: active",
    "2019-06-09 07:58:41 UTC main WARN parity_ethereum::run  Warning: Warp Sync is disabled because Fat DB is turned on.",
    "2019-06-09 07:58:41 UTC main INFO parity_ethereum::upgrade  Moved 1 keys from /opt/keys to /opt/keys/dawn",
    "2019-06-09 07:58:41 UTC main INFO ethcore_service::service  Configured for dawn using AuthorityRound engine",
    "2019-06-09 07:58:41 UTC main INFO engine  Signal for switch to contract-based validator set.",
    "2019-06-09 07:58:41 UTC main INFO engine  Initial contract validators: [0x1a8d2ae512134b640035a97330b433f075d0480c]",
    "2019-06-09 07:58:41 UTC main INFO parity_ws  Listening for new connections on 0.0.0.0:8051.",
    "2019-06-09 07:58:47 UTC IO Worker #1 INFO network  Public node URL: enode://9d83bd776c6cea1f961037ebdd0150b5ba04053038379b3c46293188052e7b98046675f6efaaea6f6851e6c5b651b9d7dd89b734564877744f3b87338090f4ca@172.31.19.91:30300",
    "2019-06-09 07:59:11 UTC IO Worker #1 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 07:59:41 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:00:11 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:00:41 UTC IO Worker #1 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:01:11 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:01:41 UTC IO Worker #1 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:02:11 UTC IO Worker #2 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:02:41 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:03:11 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:03:41 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:04:11 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:04:41 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:05:11 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:05:41 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:06:16 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:06:46 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:07:16 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:07:46 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:08:16 UTC IO Worker #2 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:08:46 UTC IO Worker #1 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:09:16 UTC IO Worker #0 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:09:46 UTC IO Worker #2 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:10:16 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:10:46 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:11:16 UTC IO Worker #2 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:11:46 UTC IO Worker #3 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs",
    "2019-06-09 08:12:16 UTC IO Worker #1 INFO import     0/25 peers      8 KiB chain   53 KiB db  0 bytes queue 448 bytes sync  RPC:  0 conn,    0 req/s,    0 µs"
]
```

Retrieve paginated logs for a network node.

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
