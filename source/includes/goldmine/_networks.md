# Networks

## List Networks

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
        "created_at": "2018-10-10T14:56:11.812732Z",
        "application_id": null,
        "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
        "name": "provide.network \"unicorn\" testnet CLONE",
        "description": null,
        "is_production": false,
        "cloneable": false,
        "enabled": true,
        "chain_id": "0x5bbe130b",
        "sidechain_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "config": {
            "block_explorer_url": null,
            "chain": null,
            "chainspec": {
                "accounts": {
                    "0x0000000000000000000000000000000000000001": {
                        "balance": "1",
                        "builtin": {
                            "name": "ecrecover",
                            "pricing": {
                                "linear": {
                                    "base": 3000,
                                    "word": 0
                                }
                            }
                        }
                    },
                    ...
                    "0x0000000000000000000000000000000000000008": {
                        "balance": "1",
                        "builtin": {
                            "activate_at": "0x0",
                            "name": "alt_bn128_pairing",
                            "pricing": {
                                "alt_bn128_pairing": {
                                    "base": 100000,
                                    "pair": 80000
                                }
                            }
                        }
                    },
                    "0x0000000000000000000000000000000000000009": {
                        "balance": "1",
                        "constructor": "0x608060405234801561001057600080fd5b50611bfe806100206000..."
                    },
                    "0x0000000000000000000000000000000000000010": {
                        "balance": "1",
                        "constructor": "0x612988610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000011": {
                        "balance": "1",
                        "constructor": "0x610876610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000012": {
                        "balance": "1",
                        "constructor": "0x610f03610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000013": {
                        "balance": "1",
                        "constructor": "0x6110cc610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000014": {
                        "balance": "1",
                        "constructor": "0x610d6b610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000015": {
                        "balance": "1",
                        "constructor": "0x61032a610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000016": {
                        "balance": "1",
                        "constructor": "0x6101db610030600b82828239805160001a60731460008114610020..."
                    },
                    "0x0000000000000000000000000000000000000017": {
                        "balance": "1",
                        "constructor": "0x60806040523480156200001157600080fd5b506040516101208062..."
                    },
                    "0x9077F27fDD606c41822f711231eEDA88317aa67a": {
                        "balance": "1"
                    }
                },
                "engine": {
                    "authorityRound": {
                        "params": {
                            "blockReward": "0xDE0B6B3A7640000",
                            "maximumUncleCount": 0,
                            "maximumUncleCountTransition": 0,
                            "stepDuration": 5,
                            "validators": {
                                "multi": {
                                    "0": {
                                        "contract": "0x0000000000000000000000000000000000000017"
                                    }
                                }
                            }
                        }
                    }
                },
                "genesis": {
                    "difficulty": "0x20000",
                    "gasLimit": "0x7A1200",
                    "seal": {
                        "authorityRound": {
                            "signature": "0x000000000000000000000000000000000000...",
                            "step": "0x0"
                        }
                    }
                },
                "name": "unicorn",
                "params": {
                    "chainID": "0x5bbe130b",
                    "eip140Transition": "0x0",
                    "eip211Transition": "0x0",
                    "eip214Transition": "0x0",
                    "eip658Transition": "0x0",
                    "gasLimitBoundDivisor": "0x400",
                    "maximumExtraDataSize": "0x20",
                    "minGasLimit": "0x1388",
                    "networkID": "0x5bbe130b"
                },
                "subprotocolName": "prvd"
            },
            "chainspec_abi": {
                "0x0000000000000000000000000000000000000017": [
                    {
                        "constant": true,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            }
                        ],
                        "name": "getValidatorSupportCount",
                        "outputs": [
                            {
                                "name": "",
                                "type": "uint256"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "view",
                        "type": "function"
                    },
                    ...
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            }
                        ],
                        "name": "removeValidator",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_app_name",
                                "type": "bytes32"
                            },
                            {
                                "name": "_version_name",
                                "type": "bytes32"
                            },
                            {
                                "name": "_init",
                                "type": "address"
                            },
                            {
                                "name": "_init_sel",
                                "type": "bytes4"
                            },
                            {
                                "name": "_init_calldata",
                                "type": "bytes"
                            },
                            {
                                "name": "_fn_sels",
                                "type": "bytes4[]"
                            },
                            {
                                "name": "_fn_addrs",
                                "type": "address[]"
                            },
                            {
                                "name": "_version_desc",
                                "type": "bytes"
                            },
                            {
                                "name": "_init_desc",
                                "type": "bytes"
                            }
                        ],
                        "name": "deployConsensus",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    ...
                    {
                        "anonymous": false,
                        "inputs": [
                            {
                                "indexed": true,
                                "name": "supporter",
                                "type": "address"
                            },
                            {
                                "indexed": true,
                                "name": "supported",
                                "type": "address"
                            },
                            {
                                "indexed": true,
                                "name": "added",
                                "type": "bool"
                            }
                        ],
                        "name": "Support",
                        "type": "event"
                    }
                ]
            },
            "chainspec_abi_url": null,
            "chainspec_url": null,
            "cloneable_cfg": {
                "_security": {
                    "egress": "*",
                    "ingress": {
                        "0.0.0.0/0": {
                            "tcp": [
                                8050,
                                8051,
                                30300
                            ],
                            "udp": [
                                30300
                            ]
                        }
                    }
                },
                "aws": {
                    "docker": {
                        "regions": {
                            "ap-northeast-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            ...
                            "us-west-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            }
                        }
                    },
                    "ubuntu-vm": {
                        "regions": {
                            "ap-northeast-1": {
                                "peer": {
                                    "0.0.9": "ami-1e22e061"
                                },
                                "validator": {
                                    "0.0.9": "ami-1e22e061"
                                }
                            },
                            ...
                            "us-west-2": {
                                "peer": {
                                    "0.0.9": "ami-813777f9"
                                },
                                "validator": {
                                    "0.0.9": "ami-813777f9"
                                }
                            }
                        }
                    }
                }
            },
            "engine_id": "authorityRound",
            "is_ethereum_network": true,
            "is_load_balanced": false,
            "json_rpc_url": null,
            "native_currency": "PRVDDOC",
            "network_id": 1539183371,
            "parity_json_rpc_url": null,
            "protocol_id": "poa",
            "websocket_url": null
        },
        "stats": null
    }
```

This endpoint enumerates available blockchain Networks and related configuration details.



## Create a Network

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks \
    -d '{"config": {
            "block_explorer_url": null,
            "chain": null,
            "chainspec": {
              "accounts": {
                "0x0000000000000000000000000000000000000001": {
                  "balance": "1",
                  "builtin": {
                    "name": "ecrecover",
                    "pricing": {
                      "linear": {
                        "base": 3000,
                        "word": 0
                      }
                    }
                  }
                },
                "0x0000000000000000000000000000000000000008": {
                  "balance": "1",
                  "builtin": {
                    "activate_at": "0x0",
                    "name": "alt_bn128_pairing",
                    "pricing": {
                      "alt_bn128_pairing": {
                        "base": 100000,
                        "pair": 80000
                      }
                    }
                  }
                },
                "0x0000000000000000000000000000000000000009": {
                  "balance": "1",
                  "constructor": "0x608060405234801561001057600080fd5b50611a7f8061..."
                },
                "0x0000000000000000000000000000000000000010": {
                  "balance": "1",
                  "constructor": "0x6116ad610030600b82828239805160001a607314600081..."
                }
              },
              "engine": {
                "authorityRound": {
                  "params": {
                    "blockReward": "0xDE0B6B3A7640000",
                    "maximumUncleCount": 0,
                    "maximumUncleCountTransition": 0,
                    "stepDuration": 5,
                    "validators": {
                      "multi": {
                        "0": {
                          "contract": "0x0000000000000000000000000000000000000018"
                        }
                      }
                    }
                  }
                }
              },
              "genesis": {
                "difficulty": "0x20000",
                "gasLimit": "0x7A1200",
                "seal": {
                  "authorityRound": {
                    "signature": "0x0000000000000000000000000000000000000000000000...",
                    "step": "0x0"
                  }
                }
              },
              "name": "unicornv2",
              "params": {
                "chainID": "0x5ba25d96",
                "eip140Transition": "0x0",
                "eip211Transition": "0x0",
                "eip214Transition": "0x0",
                "eip658Transition": "0x0",
                "gasLimitBoundDivisor": "0x400",
                "maximumExtraDataSize": "0x20",
                "minGasLimit": "0x1388",
                "networkID": "0x5ba25d96"
              },
              "subprotocolName": "prvd"
            },
            "chainspec_abi": {
              "0x0000000000000000000000000000000000000010": [
                {
                  "constant": true,
                  "inputs": null,
                  "name": "init",
                  "outputs": null,
                  "payable": false,
                  "stateMutability": "view",
                  "type": "function"
                },
                {
                  "constant": true,
                  "inputs": [
                    {
                      "name": "_storage",
                      "type": "address"
                    },
                    {
                      "name": "_exec_id",
                      "type": "bytes32"
                    },
                    {
                      "name": "_provider",
                      "type": "address"
                    }
                  ],
                  "name": "getApplications",
                  "outputs": [
                    {
                      "name": "",
                      "type": "bytes32[]"
                    }
                  ],
                  "payable": false,
                  "stateMutability": "view",
                  "type": "function"
                }
              ]
            },
            "chainspec_abi_url": null,
            "chainspec_url": null,
            "cloneable_cfg": {
              "_security": {
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
              "aws": {
                "docker": {
                  "regions": {
                    "ap-northeast-1": {
                      "peer": "providenetwork-node",
                      "validator": "providenetwork-node"
                    },
                    "ap-northeast-2": {
                      "peer": "providenetwork-node",
                      "validator": "providenetwork-node"
                    }
                  }
                },
                "ubuntu-vm": {
                  "regions": {
                    "ap-northeast-1": {
                      "peer": {
                        "0.0.9": "ami-1e22e061"
                      },
                      "validator": {
                        "0.0.9": "ami-1e22e061"
                      }
                    },
                    "ap-northeast-2": {
                      "peer": {
                        "0.0.9": "ami-bfa802d1"
                      },
                      "validator": {
                        "0.0.9": "ami-bfa802d1"
                      }
                    }
                  }
                }
              }
            },
            "engine_id": "authorityRound",
            "is_ethereum_network": true,
            "is_load_balanced": false,
            "json_rpc_url": null,
            "native_currency": "PRVD",
            "network_id": null,
            "parity_json_rpc_url": null,
            "protocol_id": "poa",
            "websocket_url": null
          },
          "name": "provide.network \"unicorn v2\" testnet clone",
          "network_id": "36a5f8e0-bfc1-49f8-a7ba-86457bb52912",
          "cloneable": false,
          "enabled": true,
          "is_production": false
        }'
HTTP/2 201
```

> Response JSON:

```json
{
  "id": "4617eb8c-4f74-4262-b626-9616ab6fa413",
  "created_at": "2018-10-15T02:22:19.585422693Z",
  "application_id": null,
  "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
  "name": "provide.network \"unicorn v2\" testnet clone",
  "description": null,
  "is_production": false,
  "cloneable": false,
  "enabled": true,
  "chain_id": "0x5bc3f9db",
  "sidechain_id": null,
  "network_id": "36a5f8e0-bfc1-49f8-a7ba-86457bb52912",
  "config": {
    "block_explorer_url": null,
    "chain": null,
    "chainspec": {
      "accounts": {
        "0x0000000000000000000000000000000000000001": {
          "balance": "1",
          "builtin": {
            "name": "ecrecover",
            "pricing": {
              "linear": {
                "base": 3000,
                "word": 0
              }
            }
          }
        },
        "0x0000000000000000000000000000000000000002": {
          "balance": "1",
          "builtin": {
            "name": "sha256",
            "pricing": {
              "linear": {
                "base": 60,
                "word": 12
              }
            }
          }
        }
      },
      "engine": {
        "authorityRound": {
          "params": {
            "blockReward": "0xDE0B6B3A7640000",
            "maximumUncleCount": 0,
            "maximumUncleCountTransition": 0,
            "stepDuration": 5,
            "validators": {
              "multi": {
                "0": {
                  "contract": "0x0000000000000000000000000000000000000018"
                }
              }
            }
          }
        }
      },
      "genesis": {
        "difficulty": "0x20000",
        "gasLimit": "0x7A1200",
        "seal": {
          "authorityRound": {
            "signature": "0x000000000000000000000000000000000000000000000000...",
            "step": "0x0"
          }
        }
      },
      "name": "unicornv2",
      "params": {
        "chainID": "0x5bc3f9db",
        "eip140Transition": "0x0",
        "eip211Transition": "0x0",
        "eip214Transition": "0x0",
        "eip658Transition": "0x0",
        "gasLimitBoundDivisor": "0x400",
        "maximumExtraDataSize": "0x20",
        "minGasLimit": "0x1388",
        "networkID": "0x5bc3f9db"
      },
      "subprotocolName": "prvd"
    },
    "chainspec_abi": {
      "0x0000000000000000000000000000000000000009": [
        {
          "anonymous": false,
          "inputs": [
            {
              "indexed": true,
              "name": "execution_id",
              "type": "bytes32"
            },
            {
              "indexed": true,
              "name": "index",
              "type": "address"
            },
            {
              "indexed": false,
              "name": "script_exec",
              "type": "address"
            }
          ],
          "name": "ApplicationInitialized",
          "type": "event"
        },
        {
          "anonymous": false,
          "inputs": [
            {
              "indexed": true,
              "name": "execution_id",
              "type": "bytes32"
            },
            {
              "indexed": true,
              "name": "script_target",
              "type": "address"
            }
          ],
          "name": "ApplicationExecution",
          "type": "event"
        }
      ],
      "0x0000000000000000000000000000000000000010": [
        {
          "constant": true,
          "inputs": null,
          "name": "init",
          "outputs": null,
          "payable": false,
          "stateMutability": "view",
          "type": "function"
        }
      ]
    },
    "chainspec_abi_url": null,
    "chainspec_url": null,
    "cloneable_cfg": {
      "_security": {
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
      "aws": {
        "docker": {
          "regions": {
            "ap-northeast-1": {
              "peer": "providenetwork-node",
              "validator": "providenetwork-node"
            },
            "ap-northeast-2": {
              "peer": "providenetwork-node",
              "validator": "providenetwork-node"
            }
          }
        },
        "ubuntu-vm": {
          "regions": {
            "ap-northeast-1": {
              "peer": {
                "0.0.9": "ami-1e22e061"
              },
              "validator": {
                "0.0.9": "ami-1e22e061"
              }
            },
            "ap-northeast-2": {
              "peer": {
                "0.0.9": "ami-bfa802d1"
              },
              "validator": {
                "0.0.9": "ami-bfa802d1"
              }
            }
          }
        }
      }
    },
    "engine_id": "authorityRound",
    "is_ethereum_network": true,
    "is_load_balanced": false,
    "json_rpc_url": null,
    "native_currency": "PRVD",
    "network_id": 1539570139,
    "parity_json_rpc_url": null,
    "protocol_id": "poa",
    "websocket_url": null
  },
  "stats": null
}
```

This endpoint creates a new `Network`. Depending on the configured protocol, certain configuration items must be present.



## Retrieve Network Details

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
    "created_at": "2018-10-10T14:56:11.812732Z",
    "application_id": null,
    "user_id": "3d9d62e8-0acf-47cd-b74f-52c1f96f8397",
    "name": "provide.network \"unicorn\" testnet CLONE",
    "description": null,
    "is_production": false,
    "cloneable": false,
    "enabled": true,
    "chain_id": "0x5bbe130b",
    "sidechain_id": null,
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "config": {
        "block_explorer_url": null,
        "chain": null,
        "chainspec": {
            "accounts": {
                "0x0000000000000000000000000000000000000001": {
                    "balance": "1",
                    "builtin": {
                        "name": "ecrecover",
                        "pricing": {
                            "linear": {
                                "base": 3000,
                                "word": 0
                            }
                        }
                    }
                },
                ...
                "0x0000000000000000000000000000000000000008": {
                    "balance": "1",
                    "builtin": {
                        "activate_at": "0x0",
                        "name": "alt_bn128_pairing",
                        "pricing": {
                            "alt_bn128_pairing": {
                                "base": 100000,
                                "pair": 80000
                            }
                        }
                    }
                },
                "0x0000000000000000000000000000000000000009": {
                    "balance": "1",
                    "constructor": "0x608060405234801561001057600080fd5b50611bfe806100206000396..."
                },
                ...
                "0x0000000000000000000000000000000000000017": {
                    "balance": "1",
                    "constructor": "0x60806040523480156200001157600080fd5b50604051610120806200a..."
                },
                "0x9077F27fDD606c41822f711231eEDA88317aa67a": {
                    "balance": "1"
                }
            },
            "engine": {
                "authorityRound": {
                    "params": {
                        "blockReward": "0xDE0B6B3A7640000",
                        "maximumUncleCount": 0,
                        "maximumUncleCountTransition": 0,
                        "stepDuration": 5,
                        "validators": {
                            "multi": {
                                "0": {
                                    "contract": "0x0000000000000000000000000000000000000017"
                                }
                            }
                        }
                    }
                }
            },
            "genesis": {
                "difficulty": "0x20000",
                "gasLimit": "0x7A1200",
                "seal": {
                    "authorityRound": {
                        "signature": "0x0000000000000000000000000000000000000000000000000000000....",
                        "step": "0x0"
                    }
                }
            },
            "name": "unicorn",
            "params": {
                "chainID": "0x5bbe130b",
                "eip140Transition": "0x0",
                "eip211Transition": "0x0",
                "eip214Transition": "0x0",
                "eip658Transition": "0x0",
                "gasLimitBoundDivisor": "0x400",
                "maximumExtraDataSize": "0x20",
                "minGasLimit": "0x1388",
                "networkID": "0x5bbe130b"
            },
            "subprotocolName": "prvd"
        },
        "chainspec_abi": {
            "0x0000000000000000000000000000000000000017": [
                {
                    "constant": true,
                    "inputs": [
                        {
                            "name": "_validator",
                            "type": "address"
                        }
                    ],
                    "name": "getValidatorSupportCount",
                    "outputs": [
                        {
                            "name": "",
                            "type": "uint256"
                        }
                    ],
                    "payable": false,
                    "stateMutability": "view",
                    "type": "function"
                },
                ...
                {
                    "anonymous": false,
                    "inputs": [
                        {
                            "indexed": true,
                            "name": "supporter",
                            "type": "address"
                        },
                        {
                            "indexed": true,
                            "name": "supported",
                            "type": "address"
                        },
                        {
                            "indexed": true,
                            "name": "added",
                            "type": "bool"
                        }
                    ],
                    "name": "Support",
                    "type": "event"
                }
            ]
        },
        "chainspec_abi_url": null,
        "chainspec_url": null,
        "cloneable_cfg": {
            "_security": {
                "egress": "*",
                "ingress": {
                    "0.0.0.0/0": {
                        "tcp": [
                            8050,
                            8051,
                            30300
                        ],
                        "udp": [
                            30300
                        ]
                    }
                }
            },
            "aws": {
                "docker": {
                    "regions": {
                        "ap-northeast-1": {
                            "peer": "providenetwork-node",
                            "validator": "providenetwork-node"
                        },
                        ...
                        "us-west-2": {
                            "peer": "providenetwork-node",
                            "validator": "providenetwork-node"
                        }
                    }
                },
                "ubuntu-vm": {
                    "regions": {
                        "ap-northeast-1": {
                            "peer": {
                                "0.0.9": "ami-1e22e061"
                            },
                            "validator": {
                                "0.0.9": "ami-1e22e061"
                            }
                        },
                        ...
                        "us-west-2": {
                            "peer": {
                                "0.0.9": "ami-813777f9"
                            },
                            "validator": {
                                "0.0.9": "ami-813777f9"
                            }
                        }
                    }
                }
            }
        },
        "engine_id": "authorityRound",
        "is_ethereum_network": true,
        "is_load_balanced": false,
        "json_rpc_url": null,
        "native_currency": "PRVDDOC",
        "network_id": 1539183371,
        "parity_json_rpc_url": null,
        "protocol_id": "poa",
        "websocket_url": null
    },
    "stats": null
}
```

This endpoint retrieves details for the given Network.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## Update a Network

```shell
curl -i -XPUT \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50 \
    -d '{"name": "provide.network \"unicorn\" testnet CLONE now with more update"}'
HTTP/2 204
```


This endpoint updates a given Network.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## Retrieve Network Status

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/transactions
HTTP/2 200
```

> Response JSON:

```json
{
    "block": 2546646,
    "chain_id": "22",
    "height": null,
    "last_block_at": 1539384240093,
    "peer_count": 0,
    "protocol_version": null,
    "state": null,
    "syncing": false,
    "meta": {
        "average_blocktime": 5.164322580645161,
        "blocktimes": [
            5.032,
            ...
            5.085
        ],
        "last_block_hash": "0xb6836eed97fd2961832f450b0b3aca0ea0df956f9c28cd5a6e281f2de483938d",
        "last_block_header": {
            "parentHash": "0x48a19fb89487ad54990840a19c06467ab0e06b01e407f13f68bc6eb70b25e83f",
            "sha3Uncles": "0x1dcc4de8dec75d7aab85b567b6ccd41ad312451b948a7413f0a142fd40d49347",
            "miner": "0x9077f27fdd606c41822f711231eeda88317aa67a",
            "stateRoot": "0x38b2dba574c7519e18af5eff4f545d7361ee497677449b4701a0d21200c5643f",
            "transactionsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
            "receiptsRoot": "0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421",
            "logsBloom": "0x0000000000000000000000000000000000000000000000000000000000000000000...",
            "difficulty": "0xfffffffffffffffffffffffffffffffe",
            "number": "0x26dbd6",
            "gasLimit": "0x47b760",
            "gasUsed": "0x0",
            "timestamp": "0x5bc123b0",
            "extraData": "0xd583010b058650617269747986312e32372e30826c69",
            "mixHash": "0x0000000000000000000000000000000000000000000000000000000000000000",
            "nonce": "0x0000000000000000",
            "hash": "0xb6836eed97fd2961832f450b0b3aca0ea0df956f9c28cd5a6e281f2de483938d"
        }
    }
}
```

This endpoint checks the status of the given Network..




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network


## List Network Addresses

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/addresses
HTTP/2 501
```

> Response JSON:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the addresses of the given Network.

<i> (Not yet implemented)</i>



### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## List Network Blocks

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/blocks
HTTP/2 501
```

> Response JSON:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the blocks of the given Network.

<i> (Not yet implemented)</i>



### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## List Network Contracts

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/contracts
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "752eadfa-f138-4c73-a9b9-822a5bfb4dc6",
        "created_at": "0001-01-01T00:00:00Z",
        "application_id": null,
        "network_id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
        "contract_id": null,
        "transaction_id": null,
        "name": "Network Contract 0x0000000000000000000000000000000000000017",
        "address": "0x0000000000000000000000000000000000000017",
        "params": null,
        "accessed_at": null
    }
```

This endpoint enumerates the contracts of the given Network.



### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## List Network Transactions

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/transactions
HTTP/2 200
```

> Response JSON:

```json
{
        "id": "f1125746-fa73-4392-a935-7a57faf3f7b0",
        "created_at": "2018-10-01T11:28:26.24501Z",
        "application_id": null,
        "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "wallet_id": "f924d014-9d76-444a-b8e1-810bd3a75319",
        "to": null,
        "value": 0,
        "data": "0x6080604052604051602080612faa833981016040818152915160008054600160a060020a0383...",
        "hash": "0x79b9bef674435c69b25f7564c2cf216b2a3640343bce2a36067016f6a3811894",
        "status": "success",
        "params": null,
        "traces": null,
        "ref": null,
        "description": null
    },
    ...
    {
        "id": "44ce12a0-3779-4e0d-b095-ca15fec0a872",
        "created_at": "2018-09-01T05:55:22.7759Z",
        "application_id": null,
        "user_id": null,
        "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "wallet_id": "dfc12196-44d8-4ca2-8e6e-46f3ccf4c3a8",
        "to": "0x139c328F1fF7910757E63F5045469CbDE18152b2",
        "value": 0,
        "data": "0x676f7fec31313233343500000000000000000000000000000000000000000000000000003031...",
        "hash": "0x8584a8a2167868c3dbd948e3eade46ae0c98ca43bdf7d7e17b0693fabf004690",
        "status": "success",
        "params": null,
        "traces": null,
        "ref": "bd90e2e8-60a4-4522-89ce-53fe0611b268",
        "description": null
    }
```

This endpoint enumerates the transactions of the given Network.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## Retrieve a Transaction

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/transactions/f1125746-fa73-4392-a935-7a57faf3f7b0
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "f1125746-fa73-4392-a935-7a57faf3f7b0",
    "created_at": "2018-10-01T11:28:26.24501Z",
    "application_id": null,
    "user_id": "7062d7f8-d536-4c53-bba5-7486a8724ac3",
    "network_id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
    "wallet_id": "f924d014-9d76-444a-b8e1-810bd3a75319",
    "to": null,
    "value": 0,
    "data": "0x6080604052604051602080612faa833981016040818152915160008054600160a060020a03831660...",
    "hash": "0x79b9bef674435c69b25f7564c2cf216b2a3640343bce2a36067016f6a3811894",
    "status": "success",
    "params": null,
    "traces": {
        "result": [
            {
                "action": {
                    "callType": null,
                    "from": "0x8cd7e456d1276e7074b10ae94dcd25f62d1ea147",
                    "gas": "0x2516fd",
                    "init": "0x6080604052604051602080612faa833981016040818152915160008054600160...",
                    "input": null,
                    "to": null,
                    "value": "0x0"
                },
                "blockHash": "0x519dd9d06775eb36d0795c469ed6892f12c5dadc881916f29cca3de9c4fd238d",
                "blockNumber": 2348545,
                "result": {
                    "address": "0x2e49f7d86daf4c3590646c4c2619b2956e8e027b",
                    "code": "0x608060405260043610620000955763ffffffff60e060020a6000350416632e9d...",
                    "gasUsed": "0x2516fd",
                    "output": null
                },
                "error": null,
                "subtraces": 0,
                "traceAddress": [],
                "transactionHash": "0x79b9bef674435c69b25f7564c2cf216b2a3640343bce2a36067016f6a3811894",
                "transactionPosition": 0,
                "type": "create"
            }
        ]
    },
    "ref": null,
    "description": null
}
```

This endpoint retrieves the details of the Network’s specified Transaction.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network
transactionId | id of the transaction

## Retrieve Network Contract

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/contracts/752eadfa-f138-4c73-a9b9-822a5bfb4dc6
HTTP/2 200
```

> Response JSON:

```json
{
    "id": "752eadfa-f138-4c73-a9b9-822a5bfb4dc6",
    "created_at": "2018-10-10T14:56:11.84238Z",
    "application_id": null,
    "network_id": "e5e0a051-6af7-4d1e-88cd-0ea1f67abd50",
    "contract_id": null,
    "transaction_id": null,
    "name": "Network Contract 0x0000000000000000000000000000000000000017",
    "address": "0x0000000000000000000000000000000000000017",
    "params": {
        "abi": [
            {
                "constant": true,
                "inputs": [
                    {
                        "name": "_validator",
                        "type": "address"
                    }
                ],
                "name": "getValidatorSupportCount",
                "outputs": [
                    {
                        "name": "",
                        "type": "uint256"
                    }
                ],
                "payable": false,
                "stateMutability": "view",
                "type": "function"
            },
            ...
            {
                "anonymous": false,
                "inputs": [
                    {
                        "indexed": true,
                        "name": "supporter",
                        "type": "address"
                    },
                    {
                        "indexed": true,
                        "name": "supported",
                        "type": "address"
                    },
                    {
                        "indexed": true,
                        "name": "added",
                        "type": "bool"
                    }
                ],
                "name": "Support",
                "type": "event"
            }
        ],
        "name": "Network Contract 0x0000000000000000000000000000000000000017"
    },
    "accessed_at": null
}
```

This endpoint retrieves the details of the Network's specified Contract.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network
contractId | The ID of the specified contract

## List Network Connectors

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/connectors
HTTP/2 501
```

> Response JSON:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the specified Network’s Connectors.

<i> (Not yet implemented)</i>



### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## List Network Bridges

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/bridges
HTTP/2 501
```

> Response JSON:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the specified Network’s Bridges.

<i> (Not yet implemented)</i>




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## List Network Oracles

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/e5e0a051-6af7-4d1e-88cd-0ea1f67abd50/oracles
```

> Response JSON:

```json
{
    "message": "not implemented"
}
```

This endpoint enumerates the specified Network’s Oracles.

<i> (Not yet implemented) </i>




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network

## List Network Token Contracts

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks/024ff1ef-7369-4dee-969c-1918c6edb5d4/tokens
HTTP/2 200
```


This endpoint enumerates the specified Network’s Tokens.




### URL Parameters

Parameter | Description
--------- | -----------
id | id of the network
