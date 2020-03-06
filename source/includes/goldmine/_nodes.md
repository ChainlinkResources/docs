# Nodes

## List Nodes

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
            "client": "parity",
            "container": "providenetwork-node",
            "default_json_rpc_port": null,
            "default_websocket_port": null,
            "engine_id": "aura",
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

List `Nodes` for a `Network`.

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
        "client":"parity",
        "container":"providenetwork-node",
        "credentials":{
            "aws_access_key_id":"AKIXXXXXXXXXXXXXXXXX",
            "aws_secret_access_key":"75yXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
        },
        "engine_id":"aura",
        "env":{
            "CHAIN_SPEC_URL":"https://www.dropbox.com/s/xbuadz3odhpux7i/spec-us-east-2.json?dl=1",
            "CLIENT":"parity",
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
        "client": "parity",
        "container": "providenetwork-node",
        "engine_id": "aura",
        "env": {
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
        "target_id": "aws"
    }
}
```

Configure a `Node` to join a specific peer-to-peer `Network`. Upon successful validation and creation of the `Node` the platform attempts to deploy it asynchronously. Depending on the `Network` (i.e., its consensus protocol, security model, etc.) and the target infrastructure (i.e., AWS, Azure or locally via Docker), various enrichment of the deployed `Node` occurs. See [Orchestration](#orchestration).

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`

### Request Parameters

Parameter | Description
--------- | -----------
config | the `Node` configuration object

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
        "client": "parity",
        "container": "providenetwork-node",
        "default_json_rpc_port": null,
        "default_websocket_port": null,
        "engine_id": "aura",
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

Retrieve details for a `Node`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | id of the `Node`

## Retreive Network Node Logs

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/ef976635-545b-46c6-9576-4e3a893a68e9/nodes/eb81ab38-4dc6-45c6-8c4d-5d5645fd3079/logs?rpp=50
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
{
    "logs":[
        {
            "timestamp":1562615957897,
            "ingest_timestamp":1562615959060,
            "message":"2019-07-08 19:59:17 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.22.44:48338."
        },
        {
            "timestamp":1562615955099,
            "ingest_timestamp":1562615959060,
            "message":"2019-07-08 19:59:15 UTC IO Worker #0 INFO import  Imported #192496 0x7aa8…ce12 (0 txs, 0.00 Mgas, 2 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615952924,
            "ingest_timestamp":1562615954058,
            "message":"2019-07-08 19:59:12 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.7.17:51298."
        },
        {
            "timestamp":1562615950156,
            "ingest_timestamp":1562615954058,
            "message":"2019-07-08 19:59:10 UTC IO Worker #1 INFO import  Imported #192495 0x4e19…cefb (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615945114,
            "ingest_timestamp":1562615949058,
            "message":"2019-07-08 19:59:05 UTC IO Worker #0 INFO import  Imported #192494 0x27be…e262 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615944439,
            "ingest_timestamp":1562615949058,
            "message":"2019-07-08 19:59:04 UTC IO Worker #1 INFO import     0/25 peers      4 MiB chain   57 KiB db  0 bytes queue 448 bytes sync  RPC:  8 conn,   39 req/s,   53 µs"
        },
        {
            "timestamp":1562615940173,
            "ingest_timestamp":1562615944062,
            "message":"2019-07-08 19:59:00 UTC IO Worker #1 INFO import  Imported #192493 0xdf5e…5dd3 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615935129,
            "ingest_timestamp":1562615939070,
            "message":"2019-07-08 19:58:55 UTC IO Worker #2 INFO import  Imported #192492 0x6528…9baf (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615930088,
            "ingest_timestamp":1562615934058,
            "message":"2019-07-08 19:58:50 UTC IO Worker #2 INFO import  Imported #192491 0xff60…1d78 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615927873,
            "ingest_timestamp":1562615929057,
            "message":"2019-07-08 19:58:47 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.22.44:48314."
        },
        {
            "timestamp":1562615925146,
            "ingest_timestamp":1562615929057,
            "message":"2019-07-08 19:58:45 UTC IO Worker #3 INFO import  Imported #192490 0xa9ec…0722 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615922897,
            "ingest_timestamp":1562615924063,
            "message":"2019-07-08 19:58:42 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.7.17:51272."
        },
        {
            "timestamp":1562615920103,
            "ingest_timestamp":1562615924063,
            "message":"2019-07-08 19:58:40 UTC IO Worker #1 INFO import  Imported #192489 0x7560…bf26 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615915061,
            "ingest_timestamp":1562615919059,
            "message":"2019-07-08 19:58:35 UTC IO Worker #0 INFO import  Imported #192488 0x37c9…7b51 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615914434,
            "ingest_timestamp":1562615919059,
            "message":"2019-07-08 19:58:34 UTC IO Worker #3 INFO import     0/25 peers      4 MiB chain   57 KiB db  0 bytes queue 448 bytes sync  RPC:  8 conn,   34 req/s,   28 µs"
        },
        {
            "timestamp":1562615910221,
            "ingest_timestamp":1562615914059,
            "message":"2019-07-08 19:58:30 UTC IO Worker #0 INFO import  Imported #192487 0x6dbc…fe99 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615905179,
            "ingest_timestamp":1562615909058,
            "message":"2019-07-08 19:58:25 UTC IO Worker #0 INFO import  Imported #192486 0xdd74…d930 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615900137,
            "ingest_timestamp":1562615904062,
            "message":"2019-07-08 19:58:20 UTC IO Worker #0 INFO import  Imported #192485 0x3d28…e3a4 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615897846,
            "ingest_timestamp":1562615899059,
            "message":"2019-07-08 19:58:17 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.22.44:48284."
        },
        {
            "timestamp":1562615895096,
            "ingest_timestamp":1562615899059,
            "message":"2019-07-08 19:58:15 UTC IO Worker #1 INFO import  Imported #192484 0x1f55…6474 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615892885,
            "ingest_timestamp":1562615894058,
            "message":"2019-07-08 19:58:12 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.7.17:51250."
        },
        {
            "timestamp":1562615890155,
            "ingest_timestamp":1562615894058,
            "message":"2019-07-08 19:58:10 UTC IO Worker #0 INFO import  Imported #192483 0x0f8d…22a4 (0 txs, 0.00 Mgas, 2 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615885111,
            "ingest_timestamp":1562615889058,
            "message":"2019-07-08 19:58:05 UTC IO Worker #2 INFO import  Imported #192482 0xa3c8…5736 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615884422,
            "ingest_timestamp":1562615889058,
            "message":"2019-07-08 19:58:04 UTC IO Worker #1 INFO import     0/25 peers      4 MiB chain   57 KiB db  0 bytes queue 448 bytes sync  RPC:  8 conn,   30 req/s,   27 µs"
        },
        {
            "timestamp":1562615880170,
            "ingest_timestamp":1562615884453,
            "message":"2019-07-08 19:58:00 UTC IO Worker #2 INFO import  Imported #192481 0xddcf…e9a5 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615875127,
            "ingest_timestamp":1562615879059,
            "message":"2019-07-08 19:57:55 UTC IO Worker #3 INFO import  Imported #192480 0x3029…d533 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615870085,
            "ingest_timestamp":1562615874060,
            "message":"2019-07-08 19:57:50 UTC IO Worker #0 INFO import  Imported #192479 0xfde4…48cb (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615867834,
            "ingest_timestamp":1562615869062,
            "message":"2019-07-08 19:57:47 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.22.44:48250."
        },
        {
            "timestamp":1562615865144,
            "ingest_timestamp":1562615869062,
            "message":"2019-07-08 19:57:45 UTC IO Worker #3 INFO import  Imported #192478 0xfbcd…a6c3 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615862860,
            "ingest_timestamp":1562615864065,
            "message":"2019-07-08 19:57:42 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.7.17:51216."
        },
        {
            "timestamp":1562615860103,
            "ingest_timestamp":1562615864065,
            "message":"2019-07-08 19:57:40 UTC IO Worker #1 INFO import  Imported #192477 0xd61e…1642 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615855160,
            "ingest_timestamp":1562615859059,
            "message":"2019-07-08 19:57:35 UTC IO Worker #1 INFO import  Imported #192476 0x94a5…4621 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615854410,
            "ingest_timestamp":1562615859059,
            "message":"2019-07-08 19:57:34 UTC IO Worker #0 INFO import     0/25 peers      4 MiB chain   57 KiB db  0 bytes queue 448 bytes sync  RPC:  8 conn,   28 req/s,   24 µs"
        },
        {
            "timestamp":1562615850119,
            "ingest_timestamp":1562615854061,
            "message":"2019-07-08 19:57:30 UTC IO Worker #3 INFO import  Imported #192475 0xd5a9…d37e (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615845177,
            "ingest_timestamp":1562615849060,
            "message":"2019-07-08 19:57:25 UTC IO Worker #2 INFO import  Imported #192474 0x156d…7941 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615840133,
            "ingest_timestamp":1562615844062,
            "message":"2019-07-08 19:57:20 UTC IO Worker #2 INFO import  Imported #192473 0x3ba7…5c0e (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615837807,
            "ingest_timestamp":1562615839061,
            "message":"2019-07-08 19:57:17 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.22.44:48226."
        },
        {
            "timestamp":1562615835090,
            "ingest_timestamp":1562615839061,
            "message":"2019-07-08 19:57:15 UTC IO Worker #3 INFO import  Imported #192472 0xf47f…a79b (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615832842,
            "ingest_timestamp":1562615834060,
            "message":"2019-07-08 19:57:12 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.7.17:51194."
        },
        {
            "timestamp":1562615830149,
            "ingest_timestamp":1562615834060,
            "message":"2019-07-08 19:57:10 UTC IO Worker #3 INFO import  Imported #192471 0x76f8…c20f (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615825104,
            "ingest_timestamp":1562615829061,
            "message":"2019-07-08 19:57:05 UTC IO Worker #2 INFO import  Imported #192470 0x89d4…4923 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615824403,
            "ingest_timestamp":1562615829061,
            "message":"2019-07-08 19:57:04 UTC IO Worker #2 INFO import     0/25 peers      4 MiB chain   57 KiB db  0 bytes queue 448 bytes sync  RPC:  8 conn,   25 req/s,   41 µs"
        },
        {
            "timestamp":1562615820155,
            "ingest_timestamp":1562615824063,
            "message":"2019-07-08 19:57:00 UTC IO Worker #0 INFO import  Imported #192469 0xe06b…9704 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615815106,
            "ingest_timestamp":1562615819061,
            "message":"2019-07-08 19:56:55 UTC IO Worker #2 INFO import  Imported #192468 0x0237…c1b4 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615810162,
            "ingest_timestamp":1562615814059,
            "message":"2019-07-08 19:56:50 UTC IO Worker #3 INFO import  Imported #192467 0x2898…8953 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615807805,
            "ingest_timestamp":1562615809060,
            "message":"2019-07-08 19:56:47 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.22.44:48192."
        },
        {
            "timestamp":1562615805119,
            "ingest_timestamp":1562615809060,
            "message":"2019-07-08 19:56:45 UTC IO Worker #1 INFO import  Imported #192466 0x069e…06a5 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615802817,
            "ingest_timestamp":1562615804062,
            "message":"2019-07-08 19:56:42 UTC  INFO parity_ws::io  Accepted a new tcp connection from 172.31.7.17:51158."
        },
        {
            "timestamp":1562615800177,
            "ingest_timestamp":1562615804062,
            "message":"2019-07-08 19:56:40 UTC IO Worker #0 INFO import  Imported #192465 0xa2d6…5c03 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        },
        {
            "timestamp":1562615795134,
            "ingest_timestamp":1562615799061,
            "message":"2019-07-08 19:56:35 UTC IO Worker #0 INFO import  Imported #192464 0x5fe2…f2d3 (0 txs, 0.00 Mgas, 1 ms, 0.57 KiB)"
        }
    ],
    "prev_token":"b/34847496690482662370648424016098991718845123603222560769",
    "next_token":"f/34847500320218853119088238595304066945135513822251646977"
}
```

Retrieve paginated logs for a network node. Currently the logs are returned sorted by descending timestamp (latest logs at the top). Paging through the logs is currently only supported by this API in that opinionated format; we may add a `sort` query parameter in the future to allow for acsending access to the logstream.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | the id of the `Node`

### Query Parameters

Parameter | Default | Description
--------- | ----- | -----------
page | n/a | page number or token indicating the next page in the log stream
rpp | 100 | number of logs to include in the response

## Update a Network Node

```shell
curl -i -XPUT \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50 \
    -d '{
    "config":{
        "client":"parity",
        "container":"providenetwork-node",
        "credentials":{
            "aws_access_key_id":"AKIXXXXXXXXXXXXXXXXX",
            "aws_secret_access_key":"77zXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
        },
        "engine_id":"aura",
        "env":{
            "CHAIN_SPEC_URL":"https://www.dropbox.com/s/xbuadz3odhpux7i/spec-us-east-2.json?dl=1",
            "CLIENT":"parity",
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
HTTP/2 204
```

Update a node. This is especially useful when credentails needed to manage underlying infrastructure are rotated. The encrypted configuration stored for the node is patched, such that any sensitive configuration items provided in the request overwrite those items in the encrypted configuration without affecting the rest of the encrypted config.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | the id of the `Node`

## Undeploy Network Node

```shell
curl -i -XDELETE \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.0LsVj7oTF0KjwbcUhg9a-fQRWB7cGzKJxLIANeX2cWE' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/nodes/59d1e7ce-3316-45b2-bf06-5fae2c6294fe
HTTP/2 204
```

Undeploy a `Node`.

### URL Parameters

Parameter | Description
--------- | -----------
id | id of the `Network`
nodeId | the id of the `Node`

## Network Node Types

Parameter | Description | Default
--------- | ----------- | -----------
config | network node configuration object | --

### Node Configuration Object

Parameter | Description | Default
--------- | ----------- | -----------
credentials | object providing vendor-specific API credentials (see examples) | --
entrypoint | array representing the container entrypoint command and its arguments | --
env | object providing environment variables to be set for the new `Node` | --
image | the Docker image from which a new container will be run; required unless the `container` parameter is provided | --
container | the vendor-specific resource (i.e., a task definition family in the case of AWS) from which a new `Node` will be run; required unless the `image` parameter is provided | --
p2p | flag indicating if the underlying container should resolve peers; if unset, peer resolution will be attempted based on the given `engine_id` and/or `role_id` parameters | n/a
provider_id | string indicating the type of underlying infrastructure or virtualization technology to be used for the deployment; should be set to `docker` at this time | --
region | any supported vendor-specific region for the deployment (i.e., `us-east-1` in the case of AWS) | --
resources | object containing target-specific `cpu`, `memory`, and `volumes` allocations | --
role | the string indicating the role for the new `Node`
security | `Security` configuration object containing egress and ingress rules for the new `Node` | --
target_id | the string representing the targeted vendor (i.e., `aws` or `azure`) | --
task_role | the optional vendor-specific task role (i.e., the ECS task execution role in the case of AWS) | --
vpc_id | the optional, vendor-specific vpc identifier | --

### Security Configuration Object

Parameter | Description | Default
--------- | ----------- | -----------
egress | mapping of IP CIDR strings to a protocol/port mapping for `Node` egress; alternatively, the value `*` may be passed instead of an object to indicate "all ports, all protocols" | --
ingress | mapping of IP CIDR strings to a protocol/port mapping for `Node` ingress; alternatively, the value `*` may be passed instead of an object to indicate "all ports, all protocols" | --
