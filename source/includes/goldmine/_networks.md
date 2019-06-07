# Networks

## List Networks

```shell
curl -i \
    -H 'Authorization: bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkYXRhIjp7fSwiZXhwIjpudWxsLCJpYXQiOjE1NTk4Nzg1NzQsImp0aSI6IjYzYTJkY2QzLWI5OTgtNDZjNC1hNzFkLTQ5MjU4YTBhYmEyMyIsInN1YiI6ImFwcGxpY2F0aW9uOmNiMjAzN2Y3LTc5ZmMtNDBmNC05NzIwLWFkYTYzNmRhNDE4MyJ9.NQLm__LbMWor-9GMG0LPcH4yQIbu9Uw70kJfRt1KP64' \
    https://goldmine.provide.services/api/v1/networks

HTTP/2 200
date: Fri, 07 Jun 2019 21:49:17 GMT
content-type: application/json; charset=UTF-8
access-control-allow-credentials: true
access-control-allow-headers: Accept, Accept-Encoding, Authorization, Cache-Control, Content-Length, Content-Type, Origin, User-Agent, X-CSRF-Token, X-Requested-With
access-control-allow-methods: GET, POST, PUT, DELETE, OPTIONS
access-control-allow-origin: *
access-control-expose-headers: X-Total-Results-Count
x-total-results-count: 5
```

> Response JSON:

```json
[
    {
        "id": "deca2436-21ba-4ff5-b225-ad1b0b2f5c59",
        "created_at": "2018-01-13T22:00:47.947907Z",
        "application_id": null,
        "user_id": null,
        "name": "Ethereum mainnet",
        "description": "Ethereum mainnet",
        "is_production": true,
        "cloneable": false,
        "enabled": true,
        "chain_id": "1",
        "sidechain_id": null,
        "network_id": null,
        "config": {
            "block_explorer_url": "https://etherscan.io",
            "chainspec_url": null,
            "cloneable_images": {},
            "is_ethereum_network": true,
            "json_rpc_url": "https://mainnet.infura.io/v3/fde5e81d5d3141a093def423db3eeb33",
            "native_currency": "ETH",
            "network_id": 1,
            "websocket_url": null,
            "infura_websocket_url": "wss://mainnet.infura.io/v3/fde5e81d5d3141a093def423db3eeb33"
        },
        "stats": null
    },
    {
        "id": "07102258-5e49-480e-86af-6d0c3260827d",
        "created_at": "2018-01-13T22:00:47.967657Z",
        "application_id": null,
        "user_id": null,
        "name": "Ethereum Rinkeby testnet",
        "description": "Rinkeby (Clique) testnet",
        "is_production": false,
        "cloneable": false,
        "enabled": true,
        "chain_id": "4",
        "sidechain_id": null,
        "network_id": null,
        "config": {
            "block_explorer_url": "https://rinkeby.etherscan.io",
            "chainspec_url": null,
            "cloneable_images": {},
            "is_ethereum_network": true,
            "json_rpc_url": "https://rinkeby.infura.io/Fzt9r5dQ6CL8ubAhBscP",
            "native_currency": "ETH",
            "network_id": 4,
            "websocket_url": null
        },
        "stats": null
    },
    {
        "id": "024ff1ef-7369-4dee-969c-1918c6edb5d4",
        "created_at": "2018-03-17T11:04:50.927964Z",
        "application_id": null,
        "user_id": null,
        "name": "provide.network \"unicorn\" testnet",
        "description": "provide.network proof-of-authority testnet",
        "is_production": false,
        "cloneable": true,
        "enabled": true,
        "chain_id": "22",
        "sidechain_id": null,
        "network_id": null,
        "config": {
            "block_explorer_url": "https://unicorn-explorer.provide.network",
            "chain": "unicorn-v0",
            "chainspec_abi_url": "https://raw.githubusercontent.com/providenetwork/chain-spec/unicorn-v0/spec.abi.json",
            "chainspec_url": "https://raw.githubusercontent.com/providenetwork/chain-spec/unicorn-v0/spec.json",
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
                            },
                            "ap-south-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ap-southeast-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ap-southeast-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ca-central-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-central-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-3": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "sa-east-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-east-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-east-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-west-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
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
                            "ap-northeast-2": {
                                "peer": {
                                    "0.0.9": "ami-bfa802d1"
                                },
                                "validator": {
                                    "0.0.9": "ami-bfa802d1"
                                }
                            },
                            "ap-south-1": {
                                "peer": {
                                    "0.0.9": "ami-6c2f0703"
                                },
                                "validator": {
                                    "0.0.9": "ami-6c2f0703"
                                }
                            },
                            "ap-southeast-1": {
                                "peer": {
                                    "0.0.9": "ami-578f8a2b"
                                },
                                "validator": {
                                    "0.0.9": "ami-578f8a2b"
                                }
                            },
                            "ap-southeast-2": {
                                "peer": {
                                    "0.0.9": "ami-ed2df18f"
                                },
                                "validator": {
                                    "0.0.9": "ami-ed2df18f"
                                }
                            },
                            "ca-central-1": {
                                "peer": {
                                    "0.0.9": "ami-8d60e3e9"
                                },
                                "validator": {
                                    "0.0.9": "ami-8d60e3e9"
                                }
                            },
                            "eu-central-1": {
                                "peer": {
                                    "0.0.9": "ami-b17c4c5a"
                                },
                                "validator": {
                                    "0.0.9": "ami-b17c4c5a"
                                }
                            },
                            "eu-west-1": {
                                "peer": {
                                    "0.0.9": "ami-86dddbff"
                                },
                                "validator": {
                                    "0.0.9": "ami-86dddbff"
                                }
                            },
                            "eu-west-2": {
                                "peer": {
                                    "0.0.9": "ami-e1799686"
                                },
                                "validator": {
                                    "0.0.9": "ami-e1799686"
                                }
                            },
                            "eu-west-3": {
                                "peer": {
                                    "0.0.9": "ami-132d9c6e"
                                },
                                "validator": {
                                    "0.0.9": "ami-132d9c6e"
                                }
                            },
                            "sa-east-1": {
                                "peer": {
                                    "0.0.9": "ami-67f6ae0b"
                                },
                                "validator": {
                                    "0.0.9": "ami-67f6ae0b"
                                }
                            },
                            "us-east-1": {
                                "peer": {
                                    "0.0.9": "ami-b55a20ca"
                                },
                                "validator": {
                                    "0.0.9": "ami-b55a20ca"
                                }
                            },
                            "us-east-2": {
                                "peer": {
                                    "0.0.9": "ami-c83c02ad"
                                },
                                "validator": {
                                    "0.0.9": "ami-c83c02ad"
                                }
                            },
                            "us-west-1": {
                                "peer": {
                                    "0.0.9": "ami-b95ebbda"
                                },
                                "validator": {
                                    "0.0.9": "ami-b95ebbda"
                                }
                            },
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
            "is_load_balanced": true,
            "json_rpc_url": "http://ec2-54-167-229-155.compute-1.amazonaws.com:8050",
            "native_currency": "PRVD",
            "network_id": 22,
            "protocol_id": "poa",
            "websocket_url": "ws://ec2-54-167-229-155.compute-1.amazonaws.com:8051"
        },
        "stats": null
    },
    {
        "id": "37cf3040-25a8-4ad2-9a88-62b423857aaf",
        "created_at": "2019-02-13T06:52:16.083483Z",
        "application_id": null,
        "user_id": null,
        "name": "xDai Chain",
        "description": "POA network xDai chain",
        "is_production": false,
        "cloneable": false,
        "enabled": true,
        "chain_id": "100",
        "sidechain_id": null,
        "network_id": null,
        "config": {
            "block_explorer_url": "https://blockscout.com/poa/dai",
            "chain": "DaiChain",
            "chainspec_abi_url": null,
            "chainspec_url": "https://raw.githubusercontent.com/poanetwork/poa-chain-spec/dai/spec.json",
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
                            },
                            "ap-south-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ap-southeast-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ap-southeast-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ca-central-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-central-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-3": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "sa-east-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-east-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-east-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-west-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
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
                            "ap-northeast-2": {
                                "peer": {
                                    "0.0.9": "ami-bfa802d1"
                                },
                                "validator": {
                                    "0.0.9": "ami-bfa802d1"
                                }
                            },
                            "ap-south-1": {
                                "peer": {
                                    "0.0.9": "ami-6c2f0703"
                                },
                                "validator": {
                                    "0.0.9": "ami-6c2f0703"
                                }
                            },
                            "ap-southeast-1": {
                                "peer": {
                                    "0.0.9": "ami-578f8a2b"
                                },
                                "validator": {
                                    "0.0.9": "ami-578f8a2b"
                                }
                            },
                            "ap-southeast-2": {
                                "peer": {
                                    "0.0.9": "ami-ed2df18f"
                                },
                                "validator": {
                                    "0.0.9": "ami-ed2df18f"
                                }
                            },
                            "ca-central-1": {
                                "peer": {
                                    "0.0.9": "ami-8d60e3e9"
                                },
                                "validator": {
                                    "0.0.9": "ami-8d60e3e9"
                                }
                            },
                            "eu-central-1": {
                                "peer": {
                                    "0.0.9": "ami-b17c4c5a"
                                },
                                "validator": {
                                    "0.0.9": "ami-b17c4c5a"
                                }
                            },
                            "eu-west-1": {
                                "peer": {
                                    "0.0.9": "ami-86dddbff"
                                },
                                "validator": {
                                    "0.0.9": "ami-86dddbff"
                                }
                            },
                            "eu-west-2": {
                                "peer": {
                                    "0.0.9": "ami-e1799686"
                                },
                                "validator": {
                                    "0.0.9": "ami-e1799686"
                                }
                            },
                            "eu-west-3": {
                                "peer": {
                                    "0.0.9": "ami-132d9c6e"
                                },
                                "validator": {
                                    "0.0.9": "ami-132d9c6e"
                                }
                            },
                            "sa-east-1": {
                                "peer": {
                                    "0.0.9": "ami-67f6ae0b"
                                },
                                "validator": {
                                    "0.0.9": "ami-67f6ae0b"
                                }
                            },
                            "us-east-1": {
                                "peer": {
                                    "0.0.9": "ami-b55a20ca"
                                },
                                "validator": {
                                    "0.0.9": "ami-b55a20ca"
                                }
                            },
                            "us-east-2": {
                                "peer": {
                                    "0.0.9": "ami-c83c02ad"
                                },
                                "validator": {
                                    "0.0.9": "ami-c83c02ad"
                                }
                            },
                            "us-west-1": {
                                "peer": {
                                    "0.0.9": "ami-b95ebbda"
                                },
                                "validator": {
                                    "0.0.9": "ami-b95ebbda"
                                }
                            },
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
            "is_load_balanced": true,
            "json_rpc_url": "https://dai-trace-ws.blockscout.com",
            "native_currency": "xDAI",
            "network_id": 22,
            "protocol_id": "poa",
            "websocket_url": "wss://dai-trace-ws.blockscout.com/ws"
        },
        "stats": null
    },
    {
        "id": "aa51a87f-f142-4341-8e94-b4b0214a009f",
        "created_at": "2019-04-26T17:04:15.761249Z",
        "application_id": null,
        "user_id": null,
        "name": "provide.network \"dawn\" testnet",
        "description": null,
        "is_production": false,
        "cloneable": false,
        "enabled": true,
        "chain_id": "0x5cc33a0f",
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
                    },
                    "0x0000000000000000000000000000000000000003": {
                        "balance": "1",
                        "builtin": {
                            "name": "ripemd160",
                            "pricing": {
                                "linear": {
                                    "base": 600,
                                    "word": 120
                                }
                            }
                        }
                    },
                    "0x0000000000000000000000000000000000000004": {
                        "balance": "1",
                        "builtin": {
                            "name": "identity",
                            "pricing": {
                                "linear": {
                                    "base": 15,
                                    "word": 3
                                }
                            }
                        }
                    },
                    "0x0000000000000000000000000000000000000005": {
                        "balance": "1",
                        "builtin": {
                            "activate_at": "0x0",
                            "name": "modexp",
                            "pricing": {
                                "modexp": {
                                    "divisor": 20
                                }
                            }
                        }
                    },
                    "0x0000000000000000000000000000000000000006": {
                        "balance": "1",
                        "builtin": {
                            "activate_at": "0x0",
                            "name": "alt_bn128_add",
                            "pricing": {
                                "linear": {
                                    "base": 500,
                                    "word": 0
                                }
                            }
                        }
                    },
                    "0x0000000000000000000000000000000000000007": {
                        "balance": "1",
                        "builtin": {
                            "activate_at": "0x0",
                            "name": "alt_bn128_mul",
                            "pricing": {
                                "linear": {
                                    "base": 40000,
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
                        "constructor": "0x608060405234801561001057600080fd5b50611bfe806100206000396000f3006080604052600436106101065763ffffffff7c010000000000000000000000000000000000000000000000000000000060003504166318b2d4a0811461010b5780631dc3e938146101cd57806321eb7ec0146101f357806327c422ee146102175780633ccfd60b146102b2578063447ddc77146102c757806347b855a414610377578063504b122f146103e257806365e60ef21461043b5780636c584dc5146104565780638bc031e1146104b757806395f84c17146104ee5780639aa4f64314610547578063a44387a41461055f578063a92f8dfb146105a9578063b8416d2e146105c1578063bb6136a9146106a5578063cce22ac9146106c9578063eb2b016d14610722575b600080fd5b34801561011757600080fd5b506101bb60048035600160a060020a0390811691602480351515926044351691369160849060643590810190830135806020601f82018190048102016040519081016040528181529291906020840183838082843750949796956020808201965090358701808201955035935083925082810201905060405190810160405280939291908181526020018383602002808284375094975061073a9650505050505050565b60405190815260200160405180910390f35b3480156101d957600080fd5b506101f1600435600160a060020a0360243516610766565b005b3480156101ff57600080fd5b506101f1600435600160a060020a03602435166107ee565b34801561022357600080fd5b50610235600435602435604435610853565b6040518515158152600160a060020a038086166020830152604082018590528316606082015260a06080820181815290820183818151815260200191508051906020019060200280838360005b8381101561029a578082015183820152602001610282565b50505050905001965050505050505060405180910390f35b3480156102be57600080fd5b506101f1610965565b3480156102d357600080fd5b506101bb60048035600160a060020a0390811691602480351515926044351691369160849060643590810190830135806020601f8201819004810201604051908101604052818152929190602084018383808284375094979695602080820196509035870180820195503593508392508281020190506040519081016040528093929190818152602001838360200280828437509497506109ab9650505050505050565b34801561038357600080fd5b5061038f600435610d3a565b60405160208082528190810183818151815260200191508051906020019060200280838360005b838110156103ce5780820151838201526020016103b6565b505050509050019250505060405180910390f35b3480156103ee57600080fd5b5061038f600480359036906044602480359081019083013580602081810201604051908101604052809392919081815260200183836020028082843750949750610dab9650505050505050565b34801561044757600080fd5b506101bb600435602435610e17565b34801561046257600080fd5b5061046e600435610e4d565b60405195151586529315156020860152911515604080860191909152600160a060020a039182166060860152918116608085015290911660a083015260c0909101905180910390f35b3480156104c357600080fd5b506104d2600435602435610e9c565b604051600160a060020a03909116815260200160405180910390f35b3480156104fa57600080fd5b506101f1600480359036906044602480359081019083013580602081810201604051908101604052809392919081815260200183836020028082843750949750610ed19650505050505050565b34801561055357600080fd5b506101f1600435611101565b34801561056b57600080fd5b50610574611201565b6040517fffffffff00000000000000000000000000000000000000000000000000000000909116815260200160405180910390f35b3480156105b557600080fd5b506101f160043561125b565b61061d60048035600160a060020a0316906024803591369160649060443590810190830135806020601f820181900481020160405190810160405281815292919060208401838380828437509497506112d99650505050505050565b60405183151581526020810183905260606040820181815290820183818151815260200191508051906020019080838360005b83811015610668578082015183820152602001610650565b50505050905090810190601f1680156106955780820380516001836020036101000a031916815260200191505b5094505050505060405180910390f35b3480156106b157600080fd5b506101bb600435600160a060020a03602435166115e0565b3480156106d557600080fd5b506101f16004803590369060446024803590810190830135806020818102016040519081016040528093929190818152602001838360200280828437509497506116029650505050505050565b34801561072e57600080fd5b506101f1600435611831565b600061074986868686866109ab565b905061075481611101565b80151561075d57fe5b95945050505050565b600082815260016020528290604090205460ff1680156107ad575060008181526001602052600160a060020a03331690604090205463010000009004600160a060020a0316145b15156107b857600080fd5b600083815260016020528290604090206002018054600160a060020a031916600160a060020a0392909216919091179055505050565b60008281526001602052600160a060020a033316906040902060010154600160a060020a03161461081e57600080fd5b600082815260016020528190604090206001018054600160a060020a031916600160a060020a03929092169190911790555050565b600080808060608180808a1580159061086b57508915155b801561087657508815155b151561088157600080fd5b6040517f6765744170704c6174657374496e666f28616464726573732c6279746573333281527f2c627974657333322c62797465733332290000000000000000000000000000006020820152603101604051809103902060008c81526001602052909350604090206002015460008c81526001602052600160a060020a039091169250604090205462010000900460ff1690506040518381523081600401526004360360048260240137600080608483865afa80151561094057600080fd5b82825260606000836020013e60a0826080015260803d0360808360a0013e3d60200182f35b33600160a060020a03166108fc30600160a060020a0316319081150290604051600060405180830381858888f193505050501580156109a8573d6000803e3d6000fd5b50565b600080546001018082558190819030604051918252600160a060020a03166c0100000000000000000000000002602082015260340160405180910390209250600080865187602001895afa801515610a0257600080fd5b3d9250506000821115610a1a57610a18836118ac565b505b60c060405190810160409081526001808352600060208085018290528b151584860152600160a060020a03808e16606087015233811660808701528b1660a086015287825291909152208151815460ff1916901515178155602082015181549015156101000261ff001990911617815560408201518154901515620100000262ff00001990911617815560608201518154600160a060020a039190911663010000000276ffffffffffffffffffffffffffffffffffffffff000000199091161781556080820151600182018054600160a060020a031916600160a060020a039290921691909117905560a08201516002919091018054600160a060020a031916600160a060020a0390921691909117905550600090505b8351811015610cd557838181518110610b4657fe5b90602001906020020151600160a060020a031633600160a060020a031614158015610b985750838181518110610b7857fe5b90602001906020020151600160a060020a031686600160a060020a031614155b8015610bcb5750838181518110610bab57fe5b90602001906020020151600160a060020a031688600160a060020a031614155b1515610bd657600080fd5b60008381526002602052604090206000858381518110610bf257fe5b90602001906020020151600160a060020a0316600160a060020a031681526020019081526020016000205415610c2757610ccd565b600083815260026020526001820190604090206000868481518110610c4857fe5b90602001906020020151600160a060020a0316600160a060020a03168152602001908152602001600020556000838152600360205260409020848281518110610c8d57fe5b906020019060200201518154600181018084556000938452919260209020018054600160a060020a031916600160a060020a039390931692909217909155505b600101610b31565b600160a060020a038616837f8901662470b70e672e9adb8cbb3627637d3fb8135adf41dd870e99c23284e731338b604051600160a060020a039283168152911660208201526040908101905180910390a3821515610d2f57fe5b505095945050505050565b6000818152600360205260609060409020805480602002602001604051908101604052809291908181526020018280548015610d9f57602002820191906000526020600020905b8154600160a060020a03168152600190910190602001808311610d81575b50505050509050919050565b60608151604051908082528060200260200182016040528015610dd8578160200160208202803883390190505b50905060405183816020015260205b8351602002602001811015610e0f576020848201208252604082205481840152602001610de7565b505092915050565b60008082604051908152602001604051809103902084604051918252602082015260409081019051809103902054949350505050565b60016020528060005260406000208054600182015460029092015460ff8083169450610100830481169362010000840490911692600160a060020a036301000000909104811692918116911686565b6003602052816000526040600020805482908110610eb657fe5b9060005260206000200154600160a060020a03169150829050565b6000828152600160205280808085604082205460ff168015610f1a575060008181526001602052600160a060020a03331690604090205463010000009004600160a060020a0316145b1515610f2557600080fd5b600094505b85518510156110f85760008781526002602052604090206000878781518110610f4f57fe5b90602001906020020151600160a060020a0316600160a060020a03168152602001908152602001600020549350831515610f88576110ed565b6000878152600260205260001990940193604090206000878781518110610fab57fe5b90602001906020020151600160a060020a0316600160a060020a03168152602001908152602001600020600090819055878152600360205260409020549250828410610ff357fe5b826001141561101a576000878152600360205260409020611015906000611b75565b6110ed565b6001840183146110cc5760008781526003602052604090208054600019850190811061104257fe5b906000526020600020015460008881526003602052600160a060020a03909116925082906040902080548690811061107657fe5b906000526020600020018054600160a060020a031916600160a060020a039290921691909117905560008781526002602052600185019060409020600160a060020a038416600090815260209190915260409020555b60008781526003602052604090208054906110eb906000198301611b91565b505b600190940193610f2a565b50505050505050565b60008181526001602052600160a060020a033316906040902060010154600160a060020a03161480156111485750600081815260016020526040902054610100900460ff16155b8015611167575060008181526001602052604090205460ff1615156001145b151561117257600080fd5b600081815260016020526040902060020154600160a060020a0316817f964b4dd912e653af365a4db23209af0af97ec08fc5ce8e3737dd2ffc62d7be8860405160405180910390a36000818152600160205260408120805460ff1916911515919091179055600081815260016020819052906040902080549115156101000261ff001990921691909117905550565b6040517f6765744170704c6174657374496e666f28616464726573732c6279746573333281527f2c627974657333322c62797465733332290000000000000000000000000000006020820152603101604051809103902081565b60008181526001602052600160a060020a03331690604090205463010000009004600160a060020a03161480156112ab575060008181526001602052604090205460ff6101009091041615156001145b15156112b657600080fd5b6000818152600160208190529060409020805460ff191691151591909117905550565b60008281526001602052806060818086604082205460ff16158015611317575060008181526001602052604090205460ff6101009091041615156001145b8015611346575060008181526001602052600160a060020a033316906040902060010154600160a060020a0316145b151561135157600080fd5b600034111561137d5760008181526001602052604090205462010000900460ff16151561137d57600080fd5b60048751101580156113975750600160a060020a03891615155b80156113a257508715155b15156113ad57600080fd5b60008881526001602052604090206001015433600160a060020a039081169116146113d757600080fd5b6000888152600260205260409020600160a060020a038a1660009081526020919091526040902054151561140a57600080fd5b6000808851896020018c5afa9550851515611467576114298989611958565b85600080604051818152601f19601f830116810160200160405290801561145a578160200160208202803883390190505b50919750955093506115d4565b60003411156115885761147988611a17565b965090935091503483111561148a57fe5b600083111561150a57600160a060020a03821683156108fc0284604051600060405180830381858888f193505050501580156114ca573d6000803e3d6000fd5b50600160a060020a038216887f1a95e881f7bd4246bed9dd2706c450a20eb432ac36963dfc77b84f60767f08368560405190815260200160405180910390a35b33600160a060020a03166108fc8434039081150290604051600060405180830381858888f19350505050158015611545573d6000803e3d6000fd5b5060408051818152601f19601f8301168101602001604052908015611574578160200160208202803883390190505b509350828460200152818460400152611594565b611591886118ac565b94505b600160a060020a038916887faf127354abdec930ef625a08ff4ae195c41e3d775821cae0222d077158108e4d60405160405180910390a38515156115d457fe5b50505093509350939050565b6002602052816000526040600020602052806000526040600020549150829050565b6000828152600160205282604082205460ff168015611648575060008181526001602052600160a060020a03331690604090205463010000009004600160a060020a0316145b151561165357600080fd5b600091505b825182101561182b57600084815260016020526040902060010154600160a060020a031683838151811061168857fe5b90602001906020020151600160a060020a0316141580156116e15750600084815260016020526040902060020154600160a060020a03168383815181106116cb57fe5b90602001906020020151600160a060020a031614155b8015611714575033600160a060020a03168383815181106116fe57fe5b90602001906020020151600160a060020a031614155b151561171f57600080fd5b6000848152600260205260409020600084848151811061173b57fe5b90602001906020020151600160a060020a0316600160a060020a03168152602001908152602001600020541561177057611820565b600084815260036020526040902083838151811061178a57fe5b906020019060200201518154600181018084556000938452919260209020018054600160a060020a031916600160a060020a03939093169290921790915550600084815260036020526040902054600085815260026020526040902060008585815181106117f457fe5b90602001906020020151600160a060020a0316600160a060020a03168152602001908152602001600020555b600190910190611658565b50505050565b60008181526001602052600160a060020a03331690604090205463010000009004600160a060020a0316148015611881575060008181526001602052604090205460ff6101009091041615156001145b151561188c57600080fd5b6000818152600160205260408120805460ff191691151591909117905550565b600060608134156118b957fe5b6118c1611b12565b915060048251101580156118e05750600282518115156118dd57fe5b06155b15156118e857fe5b5060025b81518110156119355761192d8483838151811061190557fe5b9060200190602002015184846001018151811061191e57fe5b90602001906020020151611b46565b6002016118ec565b60028083510381151561194457fe5b0492506000831161195157fe5b5050919050565b600060203d141561196f5760206000803e60005190505b80151561199957507f44656661756c74457863657074696f6e000000000000000000000000000000005b8082600160a060020a0385167f04ef79403cd298c18d57de0506ae84c75d5b563190b82ecd76d5dfcbf99ed5c360405160405180910390a46000341115611a1257600160a060020a0333163480156108fc0290604051600060405180830381858888f1935050505015801561182b573d6000803e3d6000fd5b505050565b600080600060606000611a28611b12565b91506002825110158015611a47575060028251811515611a4457fe5b06155b1515611a4f57fe5b81600081518110611a5c57fe5b90602001906020020151935081600181518110611a7557fe5b906020019060200201519450600290505b8151811015611aa757611a9f8683838151811061190557fe5b600201611a86565b600280835103811515611ab657fe5b04925030600160a060020a031684600160a060020a031614151515611ad757fe5b82151580611b01575082158015611af65750600160a060020a03841615155b8015611b0157508415155b1515611b0957fe5b50509193909250565b6060599050600060403d061115611b2857600080fd5b607f3d11611b3557600080fd5b60203d036020823e803d0160405290565b816040519081526020016040518091039020836040519182526020820152604090810190518091039020555050565b508054600082559060005260206000206109a891810190611bb1565b815481835581811115611a125781836000526020600020611a1292810191015b611bcf91905b80821115611bcb5760008155600101611bb7565b5090565b905600a165627a7a72305820bd8828d6aab33fe74cb0828381c65d24430fa414e5e9b10f9d467aad96083b460029"
                    },
                    "0x0000000000000000000000000000000000000010": {
                        "balance": "1",
                        "constructor": "0x612988610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f30073000000000000000000000000000000000000000030146080604052600436106100ba5763ffffffff7c010000000000000000000000000000000000000000000000000000000060003504166322aee80481146100bf57806323afa1d014610137578063369e220b1461022d57806346d6c207146102a45780636944f8e01461030e57806378bc449c14610370578063cfa4fe7114610433578063d53c964a14610506578063e1c7392a1461059d578063e242e018146105a7575b600080fd5b6100dd600160a060020a036004358116906024359060443516610660565b60408051838152602080820183815284519383019390935283519192916060840191858101910280838360005b8381101561012257818101518382015260200161010a565b50505050905001935050505060405180910390f35b610157600160a060020a036004351660243560443560643560843561085c565b6040518084600160a060020a0316600160a060020a03168152602001837bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19167bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1916815260200180602001828103825283818151815260200191508051906020019080838360005b838110156101f05781810151838201526020016101d8565b50505050905090810190601f16801561021d5780820380516001836020036101000a031916815260200191505b5094505050505060405180910390f35b61024a600160a060020a0360043516602435604435606435610c89565b6040518084815260200183600160a060020a0316600160a060020a031681526020018060200182810382528381815181526020019150805190602001908083836000838110156101f05781810151838201526020016101d8565b6102be600160a060020a0360043516602435604435610fbc565b60408051602080825283518183015283519192839290830191858101910280838360005b838110156102fa5781810151838201526020016102e2565b505050509050019250505060405180910390f35b61032b600160a060020a0360043516602435604435606435611193565b6040518083815260200180602001828103825283818151815260200191508051906020019060200280838360008381101561012257818101518382015260200161010a565b610390600160a060020a0360043516602435604435606435608435611392565b604051808515151515815260200184815260200183600160a060020a0316600160a060020a0316815260200180602001828103825283818151815260200191508051906020019080838360005b838110156103f55781810151838201526020016103dd565b50505050905090810190601f1680156104225780820380516001836020036101000a031916815260200191505b509550505050505060405180910390f35b610475600160a060020a03600435166024356044356064356084357bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1960a435166117ff565b6040518083600160a060020a0316600160a060020a0316815260200180602001828103825283818151815260200191508051906020019080838360005b838110156104ca5781810151838201526020016104b2565b50505050905090810190601f1680156104f75780820380516001836020036101000a031916815260200191505b50935050505060405180910390f35b610523600160a060020a0360043516602435604435606435611c4e565b60408051600160a060020a03808716825260208083018790529085169282019290925260806060820181815284519183019190915283519192909160a0840191858101910280838360005b8381101561058657818101518382015260200161056e565b505050509050019550505050505060405180910390f35b6105a56122cd565b005b6105c7600160a060020a03600435166024356044356064356084356122cf565b604051808060200180602001838103835285818151815260200191508051906020019060200280838360005b8381101561060b5781810151838201526020016105f3565b50505050905001838103825284818151815260200191508051906020019060200280838360005b8381101561064a578181015183820152602001610632565b5050505090500194505050505060405180910390f35b6000606081808080600160a060020a0389161580159061067f57508715155b80156106935750600160a060020a03871615155b151561069e57600080fd5b60408051600160a060020a0389168152815190819003602001812060008051602061293d833981519152825291519081900360150190209096506106e19061268e565b93506106ed84896126a6565b604080516000805160206128bd8339815191528152815190819003601101812060008051602061287d8339815191528252825191829003601201822089835260208084019190915283519283900384018320918352820152815190819003909101902061075b9085906126a6565b610765848a6126d1565b925082151561077357610850565b6040805160008051602061291d8339815191528152905190819003601c01902061079e908590612737565b6107a884896126a6565b6107b38460406126a6565b6107bd84846126a6565b5050604080516000805160206128bd8339815191528152815190819003601101812060008051602061287d8339815191528252825191829003601201822087835260208084019190915283519283900384018320918352820152815190819003909101902060015b8281116108435761083b846020830284016126a6565b600101610825565b61084d848a612743565b94505b50505050935093915050565b6000806060610869612845565b6000606081600160a060020a038c161580159061088557508a15155b151561089057600080fd5b891580159061089e57508815155b80156108a957508715155b15156108b457600080fd5b604080516060810180835260008051602061287d83398151915290819052825180830360720181208e825260208083019190915284519182900385019091208352600181840181905283850152835191825283519182900360120182208e83528282015283519182900384019091208252825160e060020a6361707073028152835190819003600401812083519082528183015283519081900384019020825282518c81528351908190038201812083519082528183015283519081900384019020825282516000805160206128dd8339815191528152835190819003600801812083519082528183015283519081900384019020825282518b815283519081900382018120835190825291810191909152825190819003830190208152815160008051602061291d8339815191528152915191829003601c019091209094506109fd9061268e565b9250610a09838c6126a6565b610a148360406126a6565b610a1f8360036126a6565b604080517f7665725f696e69745f61646472000000000000000000000000000000000000008152815190819003600d018120865190825260208201528151908190039091019020610a719084906126a6565b604080517f7665725f696e69745f7369676e6174757265000000000000000000000000000081528151908190036012018120865190825260208201528151908190039091019020610ac39084906126a6565b604080517f7665725f696e69745f64657363000000000000000000000000000000000000008152815190819003600d018120865190825260208201528151908190039091019020610b159084906126a6565b610b1f838d612743565b9150816000815181101515610b3057fe5b60209081029091010151825190975082906001908110610b4c57fe5b906020019060200201519550816002815181101515610b6757fe5b6020908102919091018101518582018190529081046040860152601f1615610b955760408401805160010190525b60408401511515610ba557610c7a565b6040805160008051602061291d8339815191528152905190819003601c019020610bd0908490612737565b610bda838c6126a6565b610be58360406126a6565b610bf68385604001516001026126a6565b50604080517f7665725f696e69745f64657363000000000000000000000000000000000000008152815190819003600d018120855190825260208201528151908190039091019020835260015b60408401518111610c68578351610c6090849060208402016126a6565b600101610c43565b610c778385602001518e6127b9565b94505b50505050955095509592505050565b6000806060818082818080600160a060020a038d1615801590610cab57508b15155b1515610cb657600080fd5b8a15801590610cc457508915155b1515610ccf57600080fd5b6040805160008051602061291d8339815191528152905190819003601c019020610cf89061268e565b9550610d04868d6126a6565b610d0f8660406126a6565b610d1a8660036126a6565b6040805160008051602061287d833981519152815281519081900360120181208d8252602080830191909152825191829003830182208d83528351928390038201832060e060020a6361707073028452845193849003600401842084528383019190915283519283900384018320908352828201528251918290038301822060008051602061289d8339815191528352835192839003601101832083529082018190528251918290039092019020909550610dd69087906126a6565b604080517f6170705f73746f726167655f696d706c00000000000000000000000000000000815281519081900360100181208152602081018790528151908190039091019020610e279087906126a6565b604080517f6170705f64657363000000000000000000000000000000000000000000000000815281519081900360080181208152602081018790528151908190039091019020610e789087906126a6565b610e82868e612743565b9350836000815181101515610e9357fe5b60209081029091010151845190995084906001908110610eaf57fe5b60209081029091010151845190985084906002908110610ecb57fe5b60209081029091018101519350830491506020830615610eec576001909101905b6040805160008051602061291d8339815191528152905190819003601c019020610f17908790612737565b610f21868d6126a6565b610f2c8660406126a6565b610f3686836126a6565b50604080517f6170705f646573630000000000000000000000000000000000000000000000008152815190819003600801812081526020810195909552805194859003019093209260015b818111610f9f57610f97866020830287016126a6565b600101610f81565b610faa86848f6127b9565b96505050505050509450945094915050565b60606000808080600160a060020a03881615801590610fda57508615155b8015610fe557508515155b1515610ff057600080fd5b6040805160008051602061293d833981519152815290519081900360150190206110199061268e565b935061102584886126a6565b604080516000805160206128bd8339815191528152815190819003601101812060008051602061287d833981519152825282519182900360120182208983526020808401919091528351928390038401832091835282015281519081900390910190206110939085906126a6565b61109d84896126d1565b92508215156110ab57611188565b6040805160008051602061291d8339815191528152905190819003601c0190206110d6908590612737565b6110e084886126a6565b6110eb8460406126a6565b6110f584846126a6565b5050604080516000805160206128bd8339815191528152815190819003601101812060008051602061287d8339815191528252825191829003601201822087835260208084019190915283519283900384018320918352820152815190819003909101902060015b82811161117b57611173846020830284016126a6565b60010161115d565b6111858489612743565b94505b505050509392505050565b60006060818080600160a060020a038916158015906111b157508715155b15156111bc57600080fd5b86158015906111ca57508515155b15156111d557600080fd5b6040805160008051602061293d833981519152815290519081900360150190206111fe9061268e565b925061120a83896126a6565b6040805160008051602061287d833981519152815281519081900360120181208982526020808301919091528251918290038301822060e060020a6361707073028352835192839003600401832083528282015282519182900383018220898352835192839003820183208352828201528251918290038301822060008051602061289d83398151915283528351928390036011018320835290820181905282519182900390920190209092506112c29084906126a6565b6112cc838a6126d1565b94508415156112da57611386565b6040805160008051602061291d8339815191528152905190819003601c019020611305908490612737565b61130f83896126a6565b61131a8360406126a6565b61132483866126a6565b506040805160008051602061289d833981519152815281519081900360110181208152602081019290925280519182900301902060015b84811161137957611371836020830284016126a6565b60010161135b565b611383838a612743565b93505b50505094509492505050565b600080600060606113a1612845565b6000606081600160a060020a038d16158015906113bd57508b15155b15156113c857600080fd5b8a158015906113d657508915155b80156113e157508815155b15156113ec57600080fd5b604080516060810180835260008051602061287d8339815191529052815180820360720181208e825260208083019190915283519182900384019091208252600181830181905282840152825160e060020a6361707073028152835190819003600401812083519082528183015283519081900384019020825282518d81528351908190038201812083519082528183015283519081900384019020825282516000805160206128dd8339815191528152835190819003600801812083519082528183015283519081900384019020825282518c815283519081900382018120835190825291810191909152825190819003830190208152815160008051602061291d8339815191528152915191829003601c0190912090945061150f9061268e565b925061151b838d6126a6565b6115268360406126a6565b6115318360046126a6565b604080517f7665725f69735f66696e616c697a656400000000000000000000000000000000815281519081900360100181208651908252602082015281519081900390910190206115839084906126a6565b604080517f7665725f66756e6374696f6e735f6c6973740000000000000000000000000000815281519081900360120181208651908252602082015281519081900390910190206115d59084906126a6565b604080517f7665725f73746f726167655f696d706c00000000000000000000000000000000815281519081900360100181208651908252602082015281519081900390910190206116279084906126a6565b604080517f7665725f64657363000000000000000000000000000000000000000000000000815281519081900360080181208651908252602082015281519081900390910190206116799084906126a6565b611683838e612743565b805190925060009083908290811061169757fe5b6020908102909101015183519114159850829060019081106116b557fe5b602090810290910101518251909750829060029081106116d157fe5b602090810290910101518251909650829060039081106116ed57fe5b6020908102919091018101518582018190529081046040860152601f161561171b5760408401805160010190525b6040805160008051602061291d8339815191528152905190819003601c019020611746908490612737565b611750838d6126a6565b61175b8360406126a6565b61176c8385604001516001026126a6565b50604080517f7665725f6465736300000000000000000000000000000000000000000000000081528151908190036008018120855190825260208201528151908190039091019020835260015b604084015181116117de5783516117d690849060208402016126a6565b6001016117b9565b6117ed8385602001518f6127b9565b94505050505095509550955095915050565b6000606061180b612845565b6000606081600160a060020a038c161580159061182757508a15155b151561183257600080fd5b891580159061184057508815155b801561184b57508715155b801561187557507bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19871615155b151561188057600080fd5b604080516060810180835260008051602061287d8339815191529052815180820360720181208d825260208083019190915283519182900384019091208252600181830181905282840152825160e060020a6361707073028152835190819003600490810182208451908352828401528451918290038501909120835283518d81528451908190038301812084519082528184015284519081900385019020835283516000805160206128dd8339815191528152845190819003600801812084519082528184015284519081900385019020835283518c81528451908190038301812084519082528184015284519081900385019020835283517f66756e6374696f6e7300000000000000000000000000000000000000000000008152845190819003600901812084519082528184015284519081900385019020835283517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff198c1681528451908190039091018120835190825291810191909152825190819003830190208152815160008051602061291d8339815191528152915191829003601c01909120909450611a2f9061268e565b9250611a3b838c6126a6565b611a468360406126a6565b611a518360026126a6565b604080517f66756e6374696f6e5f696d706c5f61646472000000000000000000000000000081528151908190036012018120865190825260208201528151908190039091019020611aa39084906126a6565b604080517f66756e635f64657363000000000000000000000000000000000000000000000081528151908190036009018120865190825260208201528151908190039091019020611af59084906126a6565b611aff838d612743565b9150816000815181101515611b1057fe5b60209081029091010151825190965082906001908110611b2c57fe5b6020908102919091018101518582018190529081046040860152601f1615611b5a5760408401805160010190525b60408401511515611b6a57611c3f565b6040805160008051602061291d8339815191528152905190819003601c019020611b95908490612737565b611b9f838c6126a6565b611baa8360406126a6565b611bbb8385604001516001026126a6565b50604080517f66756e635f64657363000000000000000000000000000000000000000000000081528151908190036009018120855190825260208201528151908190039091019020835260015b60408401518111611c2d578351611c2590849060208402016126a6565b600101611c08565b611c3c8385602001518e6127b9565b94505b50505050965096945050505050565b60008060006060611c5d612865565b60006060818080600160a060020a038e1615801590611c7b57508c15155b1515611c8657600080fd5b8b15801590611c9457508a15155b1515611c9f57600080fd5b6040805180820180835260008051602061287d8339815191529052815180820360520181208f825260208083019190915283519182900384019091208252600090820152815160008051602061291d8339815191528152915191829003601c01909120909650611d0e9061268e565b9450611d1a858e6126a6565b611d258560406126a6565b611d308560026126a6565b6040805160008051602061287d833981519152815281519081900360120181208e825260208083019190915282519182900383019091208852815160e060020a6361707073028152825190819003600401812089519082528183015282519081900383019020885281518d81528251908190038201812089519082528183015282519081900383019020885281517f6170705f73746f726167655f696d706c00000000000000000000000000000000815282519081900360100181208951908252918101919091528151908190039091019020611e0e9086906126a6565b6040805160008051602061289d83398151915281528151908190036011018120885190825260208201528151908190039091019020611e4e9086906126a6565b611e58858f612743565b9350836000815181101515611e6957fe5b602090810290910101518451909a5084906001908110611e8557fe5b60209081029091018101519087018190521515611ea1576122bc565b6040805160008051602061289d833981519152815281519081900360110181208851908252602080830191909152825191829003830182206000805160206128dd833981519152835283519283900360080183208a5190845283830152835192839003909301909120885287015190935091505b60008211156121a4576040805160008051602061293d83398151915281529051908190036015019020611f49908690612737565b611f53858e6126a6565b611f62856020840285016126a6565b611f6c858f6126d1565b60408051828152815190819003602090810182208a51908352908201528151908190038201812060008051602061291d8339815191528252915190819003601c019020919a509150611fbf908690612737565b611fc9858e6126a6565b611fd48560406126a6565b611fdf8560046126a6565b604080517f7665725f69735f66696e616c697a6564000000000000000000000000000000008152815190819003601001812081526020810183905281519081900390910190206120309086906126a6565b604080517f7665725f696e69745f61646472000000000000000000000000000000000000008152815190819003600d01812081526020810183905281519081900390910190206120819086906126a6565b604080516000805160206128fd8339815191528152815190819003601201812081526020810183905281519081900390910190206120c09086906126a6565b604080517f7665725f73746f726167655f696d706c000000000000000000000000000000008152815190819003601001812081526020810183905281519081900390910190206121119086906126a6565b61211b858f612743565b805190945060009085908290811061212f57fe5b60209081029091010151146121985783600181518110151561214d57fe5b6020908102909101015184519098508490600290811061216957fe5b60209081029091018101519087015283518490600390811061218757fe5b6020908102909101015199506121a4565b60001990910190611f15565b600160a060020a03881615156121c057600099508998506122bc565b602086015115156121d0576122bc565b6040805160008051602061291d8339815191528152905190819003601c0190206121fb908690612737565b612205858e6126a6565b6122108560406126a6565b6122218587602001516001026126a6565b604080518a8152815190819003602090810182208951908352828201528251918290038301909120885281516000805160206128fd8339815191528152825190819003601201812089519082529181019190915281519081900390910190208652600191505b602086015182116122af5785516122a490869060208502016126a6565b600190910190612287565b6122b9858f612743565b96505b505050505050945094509450949050565b565b606080600080828180600160a060020a038c16158015906122ef57508a15155b15156122fa57600080fd5b891580159061230857508815155b801561231357508715155b151561231e57600080fd5b6040805160008051602061287d833981519152815281519081900360120181208c82526020808301919091528251918290038301822060e060020a63617070730283528351928390036004018320835282820152825191829003830182208c835283519283900382018320835282820152825191829003830182206000805160206128dd83398151915283528351928390036008018320835282820152825191829003830182208b8352835192839003820183208352908201528151908190038201812060008051602061291d8339815191528252915190819003601c01902090955061240a9061268e565b9350612416848c6126a6565b6124218460406126a6565b61242c8460026126a6565b604080517f7665725f66756e6374696f6e735f6c697374000000000000000000000000000081528151908190036012018120815260208101879052815190819003909101902061247d9085906126a6565b604080516000805160206128fd8339815191528152815190819003601201812081526020810187905281519081900390910190206124bc9085906126a6565b6124c6848d612743565b92508260008151811015156124d757fe5b602090810290910101518351909250839060019081106124f357fe5b60209081029091010151821461250557fe5b8115156125115761267f565b6040805160008051602061291d8339815191528152905190819003601c01902061253c908590612737565b612546848c6126a6565b6125518460406126a6565b61255b84836126a6565b5060015b8181116125c457604080517f7665725f66756e6374696f6e735f6c6973740000000000000000000000000000815281519081900360120181208152602080820188905282519182900390920190206125bc918691908402016126a6565b60010161255f565b6125ce848d612743565b6040805160008051602061291d8339815191528152905190819003601c0190209097506125fa9061268e565b9350612606848c6126a6565b6126118460406126a6565b61261b84836126a6565b5060015b81811161267257604080516000805160206128fd8339815191528152815190819003601201812081526020808201889052825191829003909201902061266a918691908402016126a6565b60010161261f565b61267c848d612743565b95505b50505050509550959350505050565b60408051600481526020810192909252818101905290565b8151602001818184015280835280836020010160405110156126cc578083602c01016040525b505050565b600080604484511415156126e457600080fd5b602084855186602001865afa9050600081111561270057835191505b801515612730576127307f53746f72616765526561644661696c656400000000000000000000000000000061283b565b5092915050565b60048252602090910152565b6060600060848451101561275657600080fd5b600080855186602001865afa9050600081111561270057835160203d03111561277e57600080fd5b60203d036020853e839150801515612730576127307f53746f72616765526561644661696c656400000000000000000000000000000061283b565b606060006084855110156127cc57600080fd5b600080865187602001865afa9050600081111561280357845160203d0311156127f457600080fd5b60203d036020863e8491508382525b801515612833576128337f53746f72616765526561644661696c656400000000000000000000000000000061283b565b509392505050565b8060005260206000fd5b604080516060810182526000808252602082018190529181019190915290565b604080518082019091526000808252602082015290560072656769737472795f70726f76696465727300000000000000000000000000006170705f76657273696f6e735f6c69737400000000000000000000000000000070726f76696465725f6170705f6c69737400000000000000000000000000000076657273696f6e730000000000000000000000000000000000000000000000007665725f66756e6374696f6e5f61646472730000000000000000000000000000726561644d756c746928627974657333322c627974657333325b5d29000000007265616428627974657333322c62797465733332290000000000000000000000a165627a7a72305820bc6bbb094e673587fd7d5dcb54b6bb76ced7669b39d74e96776f697acfd003bc0029"
                    },
                    "0x0000000000000000000000000000000000000011": {
                        "balance": "1",
                        "constructor": "0x610876610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f30073000000000000000000000000000000000000000030146080604052600436106100575763ffffffff7c010000000000000000000000000000000000000000000000000000000060003504166358edb440811461005c575b600080fd5b604080516020600460443581810135601f8101849004840285018401909552848452610103948235946024803573ffffffffffffffffffffffffffffffffffffffff169536959460649492019190819084018382808284375050604080516020601f89358b018035918201839004830284018301909452808352979a9998810197919650918201945092508291508401838280828437509497506101539650505050505050565b60408051602080825283518183015283519192839290830191858101910280838360005b8381101561013f578181015183820152602001610127565b505050509050019250505060405180910390f35b6060600080600080606060008751606014151561016f57600080fd5b8a1580159061017f575060008951115b80156101a0575073ffffffffffffffffffffffffffffffffffffffff8a1615155b15156101ab57600080fd5b6101b488610684565b50604080517f726561644d756c746928627974657333322c627974657333325b5d29000000008152905190819003601c01902091975095506101f5906106d3565b935061020184876106eb565b61020c8460406106eb565b6102178460026106eb565b60408051868152815190819003602090810182207f72656769737472795f70726f76696465727300000000000000000000000000008352835192839003601201832090835282820152825191829003830182208e8352835192839003820183207f6170707300000000000000000000000000000000000000000000000000000000845284519384900360040184208452838301829052845193849003850184209084529183019190915282519182900390920190209093506102da9085906106eb565b604080517f70726f76696465725f6170705f6c69737400000000000000000000000000000081528151908190036011018120815260208101859052815190819003909101902061032b9085906106eb565b61033484610716565b805190925060009083908290811061034857fe5b6020908102909101015114610380576103807f496e73756666696369656e745065726d697373696f6e73000000000000000000610793565b81600181518110151561038f57fe5b6020908102909101015190506103a48461079d565b6103af8460006107a3565b6103ba8460006107a3565b604080518c8152815190819003602090810182207f61707073000000000000000000000000000000000000000000000000000000008352835192839003600401832083528282019690965282519182900383018220958252810194909452805193849003019092209161042d84846107a3565b610437848c6107a3565b604080517f6170705f73746f726167655f696d706c000000000000000000000000000000008152815190819003601001812081526020810185905281519081900390910190206104889085906107a3565b6104a88473ffffffffffffffffffffffffffffffffffffffff8c166107a3565b60408051868152815190819003602090810182207f72656769737472795f70726f76696465727300000000000000000000000000008352835192839003601201832090835282820152825191829003830182207f70726f76696465725f6170705f6c697374000000000000000000000000000000835283519283900360110183208352908201528151908190039091019020925061054684846107a3565b61055384600183016107a3565b6105648460208084028601016107a3565b61056e848c6107a3565b60408051868152815190819003602090810182207f72656769737472795f70726f76696465727300000000000000000000000000008352835192839003601201832090835282820152825191829003830182208e8352835192839003820183207f6170707300000000000000000000000000000000000000000000000000000000845284519384900360040184208452838301919091528351928390038401832090835282820152825191829003830182207f6170705f64657363000000000000000000000000000000000000000000000000835283519283900360080183208352908201528151908190039091019020925061066c84848b6107cd565b6106758461082a565b9b9a5050505050505050505050565b60208101516040820151606083015181158061069e575082155b156106cc576106cc7f556e6b6e6f776e436f6e74657874000000000000000000000000000000000000610793565b9193909250565b60408051600481526020810192909252818101905290565b815160200181818401528083528083602001016040511015610711578083602c01016040525b505050565b6060600060848351101561072957600080fd5b600080845185602001335afa9050600081111561075d57825160203d03111561075157600080fd5b60203d036020843e8291505b80151561078d5761078d7f53746f72616765526561644661696c6564000000000000000000000000000000610793565b50919050565b8060005260206000fd5b60009052565b81516020018181840152808352808360200101604051101561071157808360400101604052505050565b825160200160005b82516020018110156107ff57808401600282028301860190815283820151602091820152016107d5565b84518160020201855284518560200101604051101561082357845185604001016040525b5050505050565b606060006020835106111561083e57600080fd5b508051602090048152905600a165627a7a7230582030ed49c0625458e94ecc17d67c4a3a7ad0f563f9961f1a6c801194d47f9e90cc0029"
                    },
                    "0x0000000000000000000000000000000000000012": {
                        "balance": "1",
                        "constructor": "0x610f03610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f30073000000000000000000000000000000000000000030146080604052600436106100625763ffffffff7c01000000000000000000000000000000000000000000000000000000006000350416634ae962608114610067578063d6bb88c814610188575b600080fd5b604080516020601f60843560048181013592830184900484028501840190955281845261013894803594602480359573ffffffffffffffffffffffffffffffffffffffff60443516957bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19606435169536959460a494909391019190819084018382808284375050604080516020601f89358b018035918201839004830284018301909452808352979a9998810197919650918201945092508291508401838280828437509497506102329650505050505050565b60408051602080825283518183015283519192839290830191858101910280838360005b8381101561017457818101518382015260200161015c565b505050509050019250505060405180910390f35b604080516020601f60643560048181013592830184900484028501840190955281845261013894803594602480359573ffffffffffffffffffffffffffffffffffffffff60443516953695608494930191819084018382808284375050604080516020601f89358b018035918201839004830284018301909452808352979a99988101979196509182019450925082915084018382808284375094975061071f9650505050505050565b606060008060008060608651606014151561024c57600080fd5b8b1580159061025a57508a15155b151561026557600080fd5b73ffffffffffffffffffffffffffffffffffffffff8a16158015906102a857507bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19891615155b80156102b5575060008851115b15156102c057600080fd5b6102c987610d11565b50604080517f726561644d756c746928627974657333322c627974657333325b5d29000000008152905190819003601c019020919650945061030a90610d60565b92506103168386610d78565b610321836040610d78565b61032c836003610d78565b60408051858152815190819003602090810182207f72656769737472795f70726f76696465727300000000000000000000000000008352835192839003601201832090835282820152825191829003830182208f8352835192839003820183207f6170707300000000000000000000000000000000000000000000000000000000845284519384900360040184208452838301919091528351928390038401832090835290820152815190819003909101902091506103eb8383610d78565b604080518c8152815190819003602090810182207f76657273696f6e730000000000000000000000000000000000000000000000008352835192839003600801832083528282019590955282519182900383018220948252810193909352805192839003019091209061045e8383610d78565b604080517f7665725f69735f66696e616c697a6564000000000000000000000000000000008152815190819003601001812081526020810184905281519081900390910190206104af908490610d78565b6104b883610da3565b80519091506000908290829081106104cc57fe5b6020908102909101015114806104fb57508051600090829060019081106104ef57fe5b60209081029091010151145b80610520575080516000908290600290811061051357fe5b6020908102909101015114155b1561054e5761054e7f496e73756666696369656e745065726d697373696f6e73000000000000000000610e20565b61055783610e2a565b610562836000610e30565b61056d836000610e30565b604080517f7665725f69735f66696e616c697a6564000000000000000000000000000000008152815190819003601001812081526020810184905281519081900390910190206105be908490610e30565b6105c9836001610e30565b604080517f7665725f696e69745f61646472000000000000000000000000000000000000008152815190819003600d018120815260208101849052815190819003909101902061061a908490610e30565b61063a8373ffffffffffffffffffffffffffffffffffffffff8c16610e30565b604080517f7665725f696e69745f7369676e6174757265000000000000000000000000000081528151908190036012018120815260208101849052815190819003909101902061068b908490610e30565b6106b4837bffffffffffffffffffffffffffffffffffffffffffffffffffffffff198b16610e30565b604080517f7665725f696e69745f64657363000000000000000000000000000000000000008152815190819003600d01812081526020810184905281519081900390910190206107069084908a610e5a565b61070f83610eb7565b9c9b505050505050505050505050565b6060600080600080606060008751606014151561073b57600080fd5b8b1580159061074957508a15155b8015610756575060008951115b151561076157600080fd5b61076a88610d11565b50809650819750505084604051808260001916600019168152602001915050604051809103902060405180807f72656769737472795f70726f766964657273000000000000000000000000000081525060120190506040518091039020604051808360001916600019168152602001826000191660001916815260200192505050604051809103902093508b604051808260001916600019168152602001915050604051809103902060405180807f617070730000000000000000000000000000000000000000000000000000000081525060040190506040518091039020856040518083600019166000191681526020018260001916600019168152602001925050506040518091039020604051808360001916600019168152602001826000191660001916815260200192505050604051809103902093506108e260405180807f726561644d756c746928627974657333322c627974657333325b5d2900000000815250601c0190506040518091039020610d60565b92506108ee8387610d78565b6108f9836040610d78565b610904836004610d78565b61090e8385610d78565b604080518c8152815190819003602090810182207f76657273696f6e730000000000000000000000000000000000000000000000008352835192839003600801832083528282018890528351928390038401832090835290820152815190819003909101902061097f908490610d78565b604080517f6170705f73746f726167655f696d706c000000000000000000000000000000008152815190819003601001812081526020810186905281519081900390910190206109d0908490610d78565b604080517f6170705f76657273696f6e735f6c697374000000000000000000000000000000815281519081900360110181208152602081018690528151908190039091019020610a21908490610d78565b610a2a83610da3565b8051909250600090839082908110610a3e57fe5b602090810290910101511480610a6e5750815160009083906001908110610a6157fe5b6020908102909101015114155b15610a9c57610a9c7f496e73756666696369656e745065726d697373696f6e73000000000000000000610e20565b73ffffffffffffffffffffffffffffffffffffffff8a161515610ad557816002815181101515610ac857fe5b6020908102909101015199505b816003815181101515610ae457fe5b602090810290910101519050610af983610e2a565b610b04836000610e30565b610b0f836000610e30565b604080517f6170705f76657273696f6e735f6c697374000000000000000000000000000000815281519081900360110181208152602081018690528151908190039091019020610b60908490610e30565b610b6d8360018301610e30565b604080517f6170705f76657273696f6e735f6c69737400000000000000000000000000000081528151908190036011018120815260208082018790528251918290039092019020610bc79185916001850190910201610e30565b610bd1838c610e30565b604080518c8152815190819003602090810182207f76657273696f6e7300000000000000000000000000000000000000000000000083528351928390036008018320835282820197909752825191829003830182209682528101959095528051948590030190932092610c448385610e30565b610c4e838c610e30565b604080517f7665725f73746f726167655f696d706c00000000000000000000000000000000815281519081900360100181208152602081018690528151908190039091019020610c9f908490610e30565b610cbf8373ffffffffffffffffffffffffffffffffffffffff8c16610e30565b604080517f7665725f646573630000000000000000000000000000000000000000000000008152815190819003600801812081526020810195909552805194859003019093209261070683858b610e5a565b602081015160408201516060830151811580610d2b575082155b15610d5957610d597f556e6b6e6f776e436f6e74657874000000000000000000000000000000000000610e20565b9193909250565b60408051600481526020810192909252818101905290565b815160200181818401528083528083602001016040511015610d9e578083602c01016040525b505050565b60606000608483511015610db657600080fd5b600080845185602001335afa90506000811115610dea57825160203d031115610dde57600080fd5b60203d036020843e8291505b801515610e1a57610e1a7f53746f72616765526561644661696c6564000000000000000000000000000000610e20565b50919050565b8060005260206000fd5b60009052565b815160200181818401528083528083602001016040511015610d9e57808360400101604052505050565b825160200160005b8251602001811015610e8c5780840160028202830186019081528382015160209182015201610e62565b845181600202018552845185602001016040511015610eb057845185604001016040525b5050505050565b6060600060208351061115610ecb57600080fd5b508051602090048152905600a165627a7a72305820f43d421792929dffb92d43ef02480e7fffcc655992aa2b628a2e6462563f8f240029"
                    },
                    "0x0000000000000000000000000000000000000013": {
                        "balance": "1",
                        "constructor": "0x6110cc610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f30073000000000000000000000000000000000000000030146080604052600436106100625763ffffffff7c0100000000000000000000000000000000000000000000000000000000600035041663a6a0717c8114610067578063b6561fcc1461017f575b600080fd5b604080516020600460443581810135838102808601850190965280855261012f958335956024803596369695606495939492019291829185019084908082843750506040805187358901803560208181028481018201909552818452989b9a99890198929750908201955093508392508501908490808284375050604080516020601f89358b018035918201839004830284018301909452808352979a99988101979196509182019450925082915084018382808284375094975061021d9650505050505050565b60408051602080825283518183015283519192839290830191858101910280838360005b8381101561016b578181015183820152602001610153565b505050509050019250505060405180910390f35b604080516020601f60643560048181013592830184900484028501840190955281845261012f948035946024803595600160e060020a031960443516953695608494930191819084018382808284375050604080516020601f89358b018035918201839004830284018301909452808352979a999881019791965091820194509250829150840183828082843750949750610a479650505050505050565b606060008060008060606000808851606014151561023a57600080fd5b8c1580159061024857508b15155b151561025357600080fd5b89518b51148015610265575060008b51115b151561027057600080fd5b61027989610eda565b50809750819850505085604051808260001916600019168152602001915050604051809103902060405180807f72656769737472795f70726f766964657273000000000000000000000000000081525060120190506040518091039020604051808360001916600019168152602001826000191660001916815260200192505050604051809103902094508c604051808260001916600019168152602001915050604051809103902060405180807f617070730000000000000000000000000000000000000000000000000000000081525060040190506040518091039020866040518083600019166000191681526020018260001916600019168152602001925050506040518091039020604051808360001916600019168152602001826000191660001916815260200192505050604051809103902094506103f160405180807f726561644d756c746928627974657333322c627974657333325b5d2900000000815250601c0190506040518091039020610f29565b93506103fd8488610f41565b610408846040610f41565b610413846005610f41565b61041d8486610f41565b604080518d8152815190819003602090810182207f76657273696f6e73000000000000000000000000000000000000000000000000835283519283900360080183208352828201989098528251918290038301822097825281019690965280519586900301909420936104908486610f41565b604080517f7665725f69735f66696e616c697a6564000000000000000000000000000000008152815190819003601001812081526020810187905281519081900390910190206104e1908590610f41565b604080517f7665725f66756e6374696f6e735f6c6973740000000000000000000000000000815281519081900360120181208152602081018790528151908190039091019020610532908590610f41565b604080517f7665725f66756e6374696f6e5f61646472730000000000000000000000000000815281519081900360120181208152602081018790528151908190039091019020610583908590610f41565b61058c84610f6c565b80519093506000908490829081106105a057fe5b6020908102909101015114806105cf57508251600090849060019081106105c357fe5b60209081029091010151145b806105f457508251600090849060029081106105e757fe5b6020908102909101015114155b15610622576106227f496e73756666696369656e745065726d697373696f6e73000000000000000000610fe9565b82600481518110151561063157fe5b6020908102909101015183518490600390811061064a57fe5b602090810290910101511461065b57fe5b82600381518110151561066a57fe5b60209081029091010151915061067f84610ff3565b61068a846000610ff9565b610695846000610ff9565b604080517f7665725f66756e6374696f6e735f6c69737400000000000000000000000000008152815190819003601201812081526020810187905281519081900390910190206106e6908590610ff9565b6106f6848c518401600102610ff9565b604080517f7665725f66756e6374696f6e5f61646472730000000000000000000000000000815281519081900360120181208152602081018790528151908190039091019020610747908590610ff9565b610757848c518401600102610ff9565b50805b818b5101811015610a2d57604080517f7665725f66756e6374696f6e735f6c6973740000000000000000000000000000815281519081900360120181208152602080820188905282519182900390920190206107bc9186918482020101610ff9565b6107fe848c8484038151811015156107d057fe5b906020019060200201517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1916610ff9565b604080517f7665725f66756e6374696f6e5f61646472730000000000000000000000000000815281519081900360120181208152602080820188905282519182900390920190206108559186918482020101610ff9565b61088e848b84840381518110151561086957fe5b6020908102909101015173ffffffffffffffffffffffffffffffffffffffff16610ff9565b610924848c8484038151811015156108a257fe5b602090810290910181015160408051600160e060020a0319909216825280519182900360040182207f66756e6374696f6e7300000000000000000000000000000000000000000000008352815192839003600901832083528284018b905281519283900382018320908352928201929092528151908190039091019020610ff9565b610938848c8484038151811015156107d057fe5b604080517f66756e6374696f6e5f696d706c5f616464720000000000000000000000000000815290519081900360120190208b51610a119186918e9086860390811061098057fe5b602090810290910181015160408051600160e060020a0319909216825280519182900360040182207f66756e6374696f6e7300000000000000000000000000000000000000000000008352815192839003600901832083528284018c905281519283900382018320908352828401528051918290038101822093825291810192909252805191829003019020610ff9565b610a25848b84840381518110151561086957fe5b60010161075a565b610a3684611023565b9d9c50505050505050505050505050565b6060600080600080606086516060141515610a6157600080fd5b8a15801590610a6f57508915155b1515610a7a57600080fd5b600160e060020a0319891615801590610a94575060008851115b1515610a9f57600080fd5b610aa887610eda565b50809550819650505083604051808260001916600019168152602001915050604051809103902060405180807f72656769737472795f70726f766964657273000000000000000000000000000081525060120190506040518091039020604051808360001916600019168152602001826000191660001916815260200192505050604051809103902092508a604051808260001916600019168152602001915050604051809103902060405180807f61707073000000000000000000000000000000000000000000000000000000008152506004019050604051809103902084604051808360001916600019168152602001826000191660001916815260200192505050604051809103902060405180836000191660001916815260200182600019166000191681526020019250505060405180910390209250610c2060405180807f726561644d756c746928627974657333322c627974657333325b5d2900000000815250601c0190506040518091039020610f29565b9150610c2c8286610f41565b610c37826040610f41565b610c42826004610f41565b610c4c8284610f41565b604080518b8152815190819003602090810182207f76657273696f6e7300000000000000000000000000000000000000000000000083528351928390036008018320835282820196909652825191829003830182209582528101949094528051938490030190922091610cbf8284610f41565b604080517f7665725f69735f66696e616c697a656400000000000000000000000000000000815281519081900360100181208152602081018590528151908190039091019020610d10908390610f41565b60408051600160e060020a03198b16815281519081900360040181207f66756e6374696f6e73000000000000000000000000000000000000000000000082528251918290036009018220825260208083019690965282519182900383018220908252948101949094528051938490030190922091610d8e8284610f41565b610d9782610f6c565b8051909150600090829082908110610dab57fe5b602090810290910101511480610dda5750805160009082906001908110610dce57fe5b60209081029091010151145b80610dff5750805160009082906002908110610df257fe5b6020908102909101015114155b80610e235750805160009082906003908110610e1757fe5b60209081029091010151145b15610e5157610e517f496e73756666696369656e745065726d697373696f6e73000000000000000000610fe9565b610e5a82610ff3565b610e65826000610ff9565b610e70826000610ff9565b604080517f66756e635f646573630000000000000000000000000000000000000000000000815281519081900360090181208152602081018590528151908190039091019020610ec29083908a611043565b610ecb82611023565b9b9a5050505050505050505050565b602081015160408201516060830151811580610ef4575082155b15610f2257610f227f556e6b6e6f776e436f6e74657874000000000000000000000000000000000000610fe9565b9193909250565b60408051600481526020810192909252818101905290565b815160200181818401528083528083602001016040511015610f67578083602c01016040525b505050565b60606000608483511015610f7f57600080fd5b600080845185602001335afa90506000811115610fb357825160203d031115610fa757600080fd5b60203d036020843e8291505b801515610fe357610fe37f53746f72616765526561644661696c6564000000000000000000000000000000610fe9565b50919050565b8060005260206000fd5b60009052565b815160200181818401528083528083602001016040511015610f6757808360400101604052505050565b606060006020835106111561103757600080fd5b50805160209004815290565b825160200160005b8251602001811015611075578084016002820283018601908152838201516020918201520161104b565b84518160020201855284518560200101604051101561109957845185604001016040525b50505050505600a165627a7a72305820490553405f22dd071c83ad686ead7ff341e035bce01ff43f0465bacaa68e77d90029"
                    },
                    "0x0000000000000000000000000000000000000014": {
                        "balance": "1",
                        "constructor": "0x610d6b610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f30073000000000000000000000000000000000000000030146080604052600436106100a45763ffffffff7c01000000000000000000000000000000000000000000000000000000006000350416630faea4a481146100a9578063184b9559146100d257806321abdee8146101425780633e90b07614610159578063563912cd1461018c5780638036a96a146101a3578063b2cff843146101ba578063d58f3a53146101d1575b600080fd5b6100c0600160a060020a03600435166024356101fc565b60408051918252519081900360200190f35b6100f2600160a060020a03600435811690602435811690604435166102b4565b60408051602080825283518183015283519192839290830191858101910280838360005b8381101561012e578181015183820152602001610116565b505050509050019250505060405180910390f35b6100c0600160a060020a03600435166024356106ed565b610170600160a060020a036004351660243561077f565b60408051600160a060020a039092168252519081900360200190f35b6100f2600160a060020a0360043516602435610823565b6100f2600160a060020a036004351660243561091f565b610170600160a060020a0360043516602435610a19565b6101e8600160a060020a0360043516602435610abd565b604080519115158252519081900360200190f35b600080600160a060020a0384161580159061021657508215155b151561022157600080fd5b60408051600080516020610d208339815191528152905190819003601501902061024a90610b78565b90506102568184610b90565b604080517f70656e64696e675f76616c696461746f725f636f756e7400000000000000000081528151908190036017018120815290519081900360200190206102a0908290610b90565b6102aa8185610bbb565b91505b5092915050565b60606000818180600160a060020a03881615156102d057600080fd5b60408051600180825281830190925290945084602080830190803883390190505092508783600081518110151561030357fe5b600160a060020a03909216602092830290910190910152610325600080610c1a565b604080517f6d61737465725f6f665f636572656d6f6e7900000000000000000000000000008152815190819003601201812081529051908190036020019020909250610372908390610c39565b61038582600160a060020a038a16610c39565b604080517f66696e616c697a6564000000000000000000000000000000000000000000000081528151908190036009018120815290519081900360200190206103cf908390610c39565b6103da826000610c39565b604080517f76616c696461746f725f636f6e736f6c650000000000000000000000000000008152815190819003601101812081529051908190036020019020610424908390610c39565b61043782600160a060020a038916610c39565b604080517f766f74696e675f636f6e736f6c650000000000000000000000000000000000008152815190819003600e01812081529051908190036020019020610481908390610c39565b61049482600160a060020a038816610c39565b604080517f76616c696461746f725f636f756e7400000000000000000000000000000000008152815190819003600f018120815290519081900360200190206104de908390610c39565b6104e9826001610c39565b604080517f70656e64696e675f76616c696461746f725f636f756e740000000000000000008152815190819003601701812081529051908190036020019020610533908390610c39565b61053e826001610c39565b60408051600080516020610d008339815191528152815190819003600a01812081529051908190036020019020610576908390610c39565b610584828451600102610c39565b5060005b838110156106055760408051600080516020610d008339815191528152815190819003600a018120815290519081900360209081019091206105d39184916001850190910201610c39565b6105fd8284838151811015156105e557fe5b60209081029091010151600160a060020a0316610c39565b600101610588565b604080517f70656e64696e675f76616c696461746f72730000000000000000000000000000815281519081900360120181208152905190819003602001902061064f908390610c39565b61065d828451600102610c39565b5060005b838110156106d857604080517f70656e64696e675f76616c696461746f7273000000000000000000000000000081528151908190036012018120815290519081900360209081019091206106be9184916001850190910201610c39565b6106d08284838151811015156105e557fe5b600101610661565b6106e182610c63565b98975050505050505050565b600080600160a060020a0384161580159061070757508215155b151561071257600080fd5b60408051600080516020610d208339815191528152905190819003601501902061073b90610b78565b90506107478184610b90565b60408051600080516020610d008339815191528152815190819003600a018120815290519081900360200190206102a0908290610b90565b600080600160a060020a0384161580159061079957508215155b15156107a457600080fd5b60408051600080516020610d20833981519152815290519081900360150190206107cd90610b78565b90506107d98184610b90565b604080517f76616c696461746f725f636f6e736f6c6500000000000000000000000000000081528151908190036011018120815290519081900360200190206102a0908290610b90565b606060008080600160a060020a0386161580159061084057508415155b151561084b57600080fd5b61085586866106ed565b604080517f726561644d756c746928627974657333322c627974657333325b5d29000000008152905190819003601c01902090935061089390610b78565b915061089f8286610b90565b6108aa826040610b90565b6108b48284610b90565b5060005b8281101561090b5760408051600080516020610d008339815191528152815190819003600a018120815290519081900360209081019091206109039184916001850190910201610b90565b6001016108b8565b6109158287610c83565b9695505050505050565b606060008080600160a060020a0386161580159061093c57508415155b151561094757600080fd5b61095186866101fc565b604080517f726561644d756c746928627974657333322c627974657333325b5d29000000008152905190819003601c01902090935061098f90610b78565b915061099b8286610b90565b6109a6826040610b90565b6109b08284610b90565b5060005b8281101561090b57604080517f70656e64696e675f76616c696461746f727300000000000000000000000000008152815190819003601201812081529051908190036020908101909120610a119184916001850190910201610b90565b6001016109b4565b600080600160a060020a03841615801590610a3357508215155b1515610a3e57600080fd5b60408051600080516020610d2083398151915281529051908190036015019020610a6790610b78565b9050610a738184610b90565b604080517f766f74696e675f636f6e736f6c650000000000000000000000000000000000008152815190819003600e018120815290519081900360200190206102a0908290610b90565b60008080600160a060020a03851615801590610ad857508315155b1515610ae357600080fd5b60408051600080516020610d2083398151915281529051908190036015019020610b0c90610b78565b9150610b188285610b90565b604080517f66696e616c697a656400000000000000000000000000000000000000000000008152815190819003600901812081529051908190036020019020610b62908390610b90565b610b6c8286610bbb565b60011495945050505050565b60408051600481526020810192909252818101905290565b815160200181818401528083528083602001016040511015610bb6578083602c01016040525b505050565b60008060448451141515610bce57600080fd5b602084855186602001865afa90506000811115610bea57835191505b8015156102ad576102ad7f53746f72616765526561644661696c6564000000000000000000000000000000610cf5565b6040805181815260208101939093528281019190915260608201905290565b815160200181818401528083528083602001016040511015610bb657808360400101604052505050565b6060600060208351061115610c7757600080fd5b50805160209004815290565b60606000608484511015610c9657600080fd5b600080855186602001865afa90506000811115610bea57835160203d031115610cbe57600080fd5b60203d036020853e8391508015156102ad576102ad7f53746f72616765526561644661696c65640000000000000000000000000000005b8060005260206000fd0076616c696461746f7273000000000000000000000000000000000000000000007265616428627974657333322c62797465733332290000000000000000000000a165627a7a72305820a60f92122dadf64a099db710a2ad723a1df52574cee8dc95084eab59b39bca330029"
                    },
                    "0x0000000000000000000000000000000000000015": {
                        "balance": "1",
                        "constructor": "0x61032a610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f300730000000000000000000000000000000000000000301460806040526004361061008e5763ffffffff7c010000000000000000000000000000000000000000000000000000000060003504166320b27291811461009357806340a141ff146100f05780634d238c8e146100f05780637528621114610111578063c476dd4014610119578063d69f13bb14610182575b600080fd5b6100a060043515156101a6565b60408051602080825283518183015283519192839290830191858101910280838360005b838110156100dc5781810151838201526020016100c4565b505050509050019250505060405180910390f35b6100a073ffffffffffffffffffffffffffffffffffffffff6004351661022f565b6100a0610258565b604080516020600460443581810135601f81018490048402850184019095528484526100a094823573ffffffffffffffffffffffffffffffffffffffff1694602480359536959460649492019190819084018382808284375094975061026a9650505050505050565b6100a073ffffffffffffffffffffffffffffffffffffffff60043516602435610280565b6060600080836101b75760006101ba565b60015b91506101c7600080610294565b604080517f66696e616c697a6564000000000000000000000000000000000000000000000081528151908190036009018120815290519081900360200190209091506102149082906102b3565b61021e81836102b3565b610227816102de565b949350505050565b606073ffffffffffffffffffffffffffffffffffffffff8216151561025357600080fd5b919050565b60408051600081526020810190915290565b5050604080516000815260208101909152919050565b505060408051600081526020810190915290565b6040805181815260208101939093528281019190915260608201905290565b8151602001818184015280835280836020010160405110156102d9578083604001016040525b505050565b60606000602083510611156102f257600080fd5b508051602090048152905600a165627a7a72305820bf191a0cb30210ccecb5b18d4c640b7a8b4e307ad6f34b92737b13ded640813f0029"
                    },
                    "0x0000000000000000000000000000000000000016": {
                        "balance": "1",
                        "constructor": "0x6101db610030600b82828239805160001a6073146000811461002057610022565bfe5b5030600052607381538281f30073000000000000000000000000000000000000000030146080604052600436106100625763ffffffff7c0100000000000000000000000000000000000000000000000000000000600035041663677356b48114610067578063730ad4541461012e575b600080fd5b604080516020601f6084356004818101359283018490048402850184019095528184526100de9473ffffffffffffffffffffffffffffffffffffffff81358116956024803590921695604435956064359536959460a494939101919081908401838280828437509497506101579650505050505050565b60408051602080825283518183015283519192839290830191858101910280838360005b8381101561011a578181015183820152602001610102565b505050509050019250505060405180910390f35b6100de60043573ffffffffffffffffffffffffffffffffffffffff602435166044351515610184565b606073ffffffffffffffffffffffffffffffffffffffff8616151561017b57600080fd5b95945050505050565b606073ffffffffffffffffffffffffffffffffffffffff831615156101a857600080fd5b93925050505600a165627a7a72305820ea7f3b5344218d1c46813781addfbf6291ba99417ddf7abcea7b6f53aacda4f10029"
                    },
                    "0x0000000000000000000000000000000000000017": {
                        "balance": "1",
                        "constructor": "0x60806040523480156200001157600080fd5b50604051610120806200a3a2833981018060405281019080805190602001909291908051906020019092919080519060200190929190805190602001909291908051906020019092919080519060200190929190805190602001909291908051906020019092919080519060200190929190505050886000806101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff160217905550620000e488888888886200010f640100000000026401000000009004565b62000100838383620008ca640100000000026401000000009004565b50505050505050505062001fbb565b60008060008060006001026200012462001faa565b808573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018260001916600019168152602001945050505050604051809103906000f080158015620001ec573d6000803e3d6000fd5b50600160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff160217905550600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1690508073ffffffffffffffffffffffffffffffffffffffff16638f283970306040518263ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001915050600060405180830381600087803b158015620002ee57600080fd5b505af115801562000303573d6000803e3d6000fd5b505050508073ffffffffffffffffffffffffffffffffffffffff1663914bedf43073ffffffffffffffffffffffffffffffffffffffff1660010260405180826000191660001916815260200191505060405180910390206040518263ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808260001916600019168152602001915050600060405180830381600087803b158015620003b557600080fd5b505af1158015620003ca573d6000803e3d6000fd5b505050508073ffffffffffffffffffffffffffffffffffffffff1663c50c97d0876040518263ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001915050600060405180830381600087803b1580156200046a57600080fd5b505af11580156200047f573d6000803e3d6000fd5b505050508073ffffffffffffffffffffffffffffffffffffffff1663326220bf306040518263ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001915050600060405180830381600087803b1580156200051f57600080fd5b505af115801562000534573d6000803e3d6000fd5b505050508073ffffffffffffffffffffffffffffffffffffffff16634ff45010868686866040518563ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001945050505050602060405180830381600087803b1580156200067057600080fd5b505af115801562000685573d6000803e3d6000fd5b505050506040513d60208110156200069c57600080fd5b8101908080519060200190929190505050600281600019169055506000600102600019166002546000191614151515620006d557600080fd5b600254600019168173ffffffffffffffffffffffffffffffffffffffff167fc53d75bedde5d06c2efc84d364e0fa8627a0b4af9baedfc2f5ec6a5cfc758d9560405160405180910390a38073ffffffffffffffffffffffffffffffffffffffff16636c5ccc147f4175726100000000000000000000000000000000000000000000000000000000608060405190810160405280605a81526020017f50726f6f662d6f662d617574686f7269747920636f6e73656e7375732070726f81526020017f746f636f6c20696d706c656d656e74696e672074686520617574686f7269747981526020017f20726f756e6420636f6e73656e73757320616c676f726974686d0000000000008152506040518363ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180836000191660001916815260200180602001828103825283818151815260200191508051906020019080838360005b838110156200085a5780820151818401526020810190506200083d565b50505050905090810190601f168015620008885780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015620008a957600080fd5b505af1158015620008be573d6000803e3d6000fd5b50505050505050505050565b60608060606002604051908082528060200260200182016040528015620009005781602001602082028038833980820191505090505b50925060405180807f61646456616c696461746f722861646472657373290000000000000000000000815250601501905060405180910390208360008151811015156200094957fe5b906020019060200201907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff191690817bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19168152505060405180807f61646450726f706f73616c28616464726573732c616464726573732c75696e7481526020017f2c75696e742c6279746573290000000000000000000000000000000000000000815250602c019050604051809103902083600181518110151562000a0357fe5b906020019060200201907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff191690817bffffffffffffffffffffffffffffffffffffffffffffffffffffffff191681525050600260405190808252806020026020018201604052801562000a825781602001602082028038833980820191505090505b5091508482600081518110151562000a9657fe5b9060200190602002019073ffffffffffffffffffffffffffffffffffffffff16908173ffffffffffffffffffffffffffffffffffffffff16815250508382600181518110151562000ae357fe5b9060200190602002019073ffffffffffffffffffffffffffffffffffffffff16908173ffffffffffffffffffffffffffffffffffffffff168152505060405180807f696e697428616464726573732c616464726573732c6164647265737329000000815250601d01905060405180910390206000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff16866000604051602401808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019350505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff8381831617835250505050905062000d7c7f41757261000000000000000000000000000000000000000000000000000000007f302e302e310000000000000000000000000000000000000000000000000000008860405180807f696e697428616464726573732c616464726573732c6164647265737329000000815250601d01905060405180910390208588886040805190810160405280601f81526020017f416c70686120617574686f7269747920726f756e6420636f6e73656e737573008152506040805190810160405280601381526020017f44656661756c7420696e697469616c697a65720000000000000000000000000081525062000d84640100000000026401000000009004565b505050505050565b6000806000606080600073ffffffffffffffffffffffffffffffffffffffff1662000dbd62001808640100000000026401000000009004565b73ffffffffffffffffffffffffffffffffffffffff1614945062000def62001adf640100000000026401000000009004565b9350600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16638f1d264f8f8f600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801562000eb857600080fd5b505af115801562000ecd573d6000803e3d6000fd5b505050506040513d602081101562000ee457600080fd5b81019080805190602001909291905050508b6040518563ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180856000191660001916815260200184600019166000191681526020018373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b8381101562000fb157808201518184015260208101905062000f94565b50505050905090810190601f16801562000fdf5780820380516001836020036101000a031916815260200191505b5095505050505050600060405180830381600087803b1580156200100257600080fd5b505af115801562001017573d6000803e3d6000fd5b50505050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16632d658f468f8f8c8c6040518563ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180856000191660001916815260200184600019166000191681526020018060200180602001838103835285818151815260200191508051906020019060200280838360005b83811015620010ed578082015181840152602081019050620010d0565b50505050905001838103825284818151815260200191508051906020019060200280838360005b838110156200113157808201518184015260208101905062001114565b505050509050019650505050505050600060405180830381600087803b1580156200115b57600080fd5b505af115801562001170573d6000803e3d6000fd5b505050508480620011ad5750600073ffffffffffffffffffffffffffffffffffffffff168473ffffffffffffffffffffffffffffffffffffffff16145b15620011d857620011d28e8e8e8e8e8b62001c76640100000000026401000000009004565b620017f8565b600073ffffffffffffffffffffffffffffffffffffffff168473ffffffffffffffffffffffffffffffffffffffff16141515620017f75760405180807f66696e616c697a65436f6e73656e73757356657273696f6e286279746573333281526020017f2c627974657333322c616464726573732c6279746573342c62797465732c627981526020017f7465732900000000000000000000000000000000000000000000000000000000815250604401905060405180910390209250828e8e8e8e8e8b60405160240180876000191660001916815260200186600019166000191681526020018573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001847bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19167bffffffffffffffffffffffffffffffffffffffffffffffffffffffff191681526020018060200180602001838103835285818151815260200191508051906020019080838360005b838110156200137557808201518184015260208101905062001358565b50505050905090810190601f168015620013a35780820380516001836020036101000a031916815260200191505b50838103825284818151815260200191508051906020019080838360005b83811015620013de578082015181840152602081019050620013c1565b50505050905090810190601f1680156200140c5780820380516001836020036101000a031916815260200191505b5098505050505050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff8381831617835250505050915060405180807f61646450726f706f73616c28616464726573732c616464726573732c75696e7481526020017f2c75696e742c6279746573290000000000000000000000000000000000000000815250602c0190506040518091039020338543600086604051602401808673ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018481526020018360ff16815260200180602001828103825283818151815260200191508051906020019080838360005b838110156200159057808201518184015260208101905062001573565b50505050905090810190601f168015620015be5780820380516001836020036101000a031916815260200191505b509650505050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c285836040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b8381101562001705578082015181840152602081019050620016e8565b50505050905090810190601f168015620017335780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b1580156200175457600080fd5b505af115801562001769573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f8201168201806040525060408110156200179457600080fd5b81019080805190602001909291908051640100000000811115620017b757600080fd5b82810190506020810184811115620017ce57600080fd5b8151856001820283011164010000000082111715620017ec57600080fd5b505092919050505050505b5b5050505050505050505050505050565b6000806000806000806060600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b1580156200189a57600080fd5b505af1158015620018af573d6000803e3d6000fd5b505050506040513d6020811015620018c657600080fd5b81019080805190602001909291905050509550600073ffffffffffffffffffffffffffffffffffffffff168673ffffffffffffffffffffffffffffffffffffffff1614151562001ad6573073ffffffffffffffffffffffffffffffffffffffff16600102604051808260001916600019168152602001915050604051809103902094508573ffffffffffffffffffffffffffffffffffffffff166327c422ee600254877f41757261000000000000000000000000000000000000000000000000000000006040518463ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808460001916600019168152602001836000191660001916815260200182600019166000191681526020019350505050600060405180830381600087803b15801562001a0357600080fd5b505af115801562001a18573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f8201168201806040525060a081101562001a4357600080fd5b8101908080519060200190929190805190602001909291908051906020019092919080519060200190929190805164010000000081111562001a8457600080fd5b8281019050602081018481111562001a9b57600080fd5b815185602082028301116401000000008211171562001ab957600080fd5b5050929190505050809550819b5082965083975084985050505050505b50505050505090565b600080600080600060405180807f676574566f74696e67436f6e736f6c6528616464726573732c6279746573333281526020017f290000000000000000000000000000000000000000000000000000000000000081525060210190506040518091039020935062001b5e62001808640100000000026401000000009004565b9250600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801562001be757600080fd5b505af115801562001bfc573d6000803e3d6000fd5b505050506040513d602081101562001c1357600080fd5b8101908080519060200190929190505050915060035490506000600102600019168160001916141562001c4a576000945062001c6f565b604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b6000600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1690508073ffffffffffffffffffffffffffffffffffffffff1663ed7870c388888888876040518663ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180866000191660001916815260200185600019166000191681526020018473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001837bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19167bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1916815260200180602001828103825283818151815260200191508051906020019080838360005b8381101562001dbd57808201518184015260208101905062001da0565b50505050905090810190601f16801562001deb5780820380516001836020036101000a031916815260200191505b509650505050505050600060405180830381600087803b15801562001e0f57600080fd5b505af115801562001e24573d6000803e3d6000fd5b505050508073ffffffffffffffffffffffffffffffffffffffff166331511bf0886000866040518463ffffffff167c01000000000000000000000000000000000000000000000000000000000281526004018084600019166000191681526020018315151515815260200180602001828103825283818151815260200191508051906020019080838360005b8381101562001ecd57808201518184015260208101905062001eb0565b50505050905090810190601f16801562001efb5780820380516001836020036101000a031916815260200191505b50945050505050606060405180830381600087803b15801562001f1d57600080fd5b505af115801562001f32573d6000803e3d6000fd5b505050506040513d606081101562001f4957600080fd5b81019080805190602001909291908051906020019092919080519060200190929190505050909150905060036000829190509060001916905550600060010260001916600354600019161415151562001fa157600080fd5b50505050505050565b6040516139538062006a4f83390190565b614a848062001fcb6000396000f3006080604052600436106100c5576000357c0100000000000000000000000000000000000000000000000000000000900463ffffffff1680631fcc449e146100ca57806340a141ff146101215780634ceefde8146101645780634d238c8e1461034457806355c1bbef146103875780636b28a5e4146103b25780637071688a146103e1578063752862111461040c578063b7ab4db514610423578063c476dd401461048f578063d69f13bb14610522578063eebc7a391461056f578063fa81b200146105db575b600080fd5b3480156100d657600080fd5b5061010b600480360381019080803573ffffffffffffffffffffffffffffffffffffffff169060200190929190505050610632565b6040518082815260200191505060405180910390f35b34801561012d57600080fd5b50610162600480360381019080803573ffffffffffffffffffffffffffffffffffffffff16906020019092919050505061079c565b005b34801561017057600080fd5b5061034260048036038101908080356000191690602001909291908035600019169060200190929190803573ffffffffffffffffffffffffffffffffffffffff16906020019092919080357bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19169060200190929190803590602001908201803590602001908080601f01602080910402602001604051908101604052809392919081815260200183838082843782019150505050505091929192908035906020019082018035906020019080806020026020016040519081016040528093929190818152602001838360200280828437820191505050505050919291929080359060200190820180359060200190808060200260200160405190810160405280939291908181526020018383602002808284378201915050505050509192919290803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290803590602001908201803590602001908080601f01602080910402602001604051908101604052809392919081815260200183838082843782019150505050505091929192905050506111fb565b005b34801561035057600080fd5b50610385600480360381019080803573ffffffffffffffffffffffffffffffffffffffff169060200190929190505050611c28565b005b34801561039357600080fd5b5061039c6123b3565b6040518082815260200191505060405180910390f35b3480156103be57600080fd5b506103c761255c565b604051808215151515815260200191505060405180910390f35b3480156103ed57600080fd5b506103f66126d8565b6040518082815260200191505060405180910390f35b34801561041857600080fd5b50610421612881565b005b34801561042f57600080fd5b50610438612f47565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b8381101561047b578082015181840152602081019050610460565b505050509050019250505060405180910390f35b34801561049b57600080fd5b50610520600480360381019080803573ffffffffffffffffffffffffffffffffffffffff16906020019092919080359060200190929190803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290505050613162565b005b34801561052e57600080fd5b5061056d600480360381019080803573ffffffffffffffffffffffffffffffffffffffff1690602001909291908035906020019092919050505061363d565b005b34801561057b57600080fd5b50610584613bb2565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b838110156105c75780820151818401526020810190506105ac565b505050509050019250505060405180910390f35b3480156105e757600080fd5b506105f0613d5a565b604051808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200191505060405180910390f35b600080600080600060405180807f67657456616c696461746f7228616464726573732c627974657333322c61646481526020017f72657373290000000000000000000000000000000000000000000000000000008152506025019050604051809103902093506106a0613d7f565b9250600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801561072857600080fd5b505af115801561073c573d6000803e3d6000fd5b505050506040513d602081101561075257600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152868160440152600080604483875afa86602060003e505050505050919050565b600060606000806060806060808860008060008060006107ba613d7f565b945060405180807f67657456616c696461746f7228616464726573732c627974657333322c61646481526020017f726573732900000000000000000000000000000000000000000000000000000081525060250190506040518091039020935060006001029250600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b1580156108a757600080fd5b505af11580156108bb573d6000803e3d6000fd5b505050506040513d60208110156108d157600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152868160440152600080604483895afa84602060903e50506001800260001916836000191614151561092b57600080fd5b6109348f610632565b9d5061093e613bb2565b9c5060018d51039b508c8c81518110151561095557fe5b906020019060200201519a508a8d8f81518110151561097057fe5b9060200190602002019073ffffffffffffffffffffffffffffffffffffffff16908173ffffffffffffffffffffffffffffffffffffffff168152505060405180807f73657456616c696461746f72496e64657828616464726573732c75696e742900815250601f01905060405180910390208b8f604051602401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200182815260200192505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509950600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c2610acc61404c565b8c6040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015610b6a578082015181840152602081019050610b4f565b50505050905090810190601f168015610b975780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015610bb757600080fd5b505af1158015610bcb573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f820116820180604052506040811015610bf557600080fd5b81019080805190602001909291908051640100000000811115610c1757600080fd5b82810190506020810184811115610c2d57600080fd5b8151856001820283011164010000000082111715610c4a57600080fd5b5050929190505050505060018d5103604051908082528060200260200182016040528015610c875781602001602082028038833980820191505090505b5098508c985060405180807f73657450656e64696e6756616c696461746f727328616464726573735b5d2900815250601f0190506040518091039020896040516024018080602001828103825283818151815260200191508051906020019060200280838360005b83811015610d0a578082015181840152602081019050610cef565b5050505090500192505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509750600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c2610dba61404c565b8a6040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015610e58578082015181840152602081019050610e3d565b50505050905090810190601f168015610e855780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015610ea557600080fd5b505af1158015610eb9573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f820116820180604052506040811015610ee357600080fd5b81019080805190602001909291908051640100000000811115610f0557600080fd5b82810190506020810184811115610f1b57600080fd5b8151856001820283011164010000000082111715610f3857600080fd5b5050929190505050505060405180807f72656d6f766556616c696461746f722861646472657373290000000000000000815250601801905060405180910390208f604051602401808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001915050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509650600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c261105a61404c565b896040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b838110156110f85780820151818401526020810190506110dd565b50505050905090810190601f1680156111255780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b15801561114557600080fd5b505af1158015611159573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f82011682018060405250604081101561118357600080fd5b810190808051906020019092919080516401000000008111156111a557600080fd5b828101905060208101848111156111bb57600080fd5b81518560018202830111640100000000821117156111d857600080fd5b505092919050505050506111ea6141cd565b505050505050505050505050505050565b6000806000606080600073ffffffffffffffffffffffffffffffffffffffff16611223613d7f565b73ffffffffffffffffffffffffffffffffffffffff161494506112446145af565b9350600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16638f1d264f8f8f600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801561130c57600080fd5b505af1158015611320573d6000803e3d6000fd5b505050506040513d602081101561133657600080fd5b81019080805190602001909291905050508b6040518563ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180856000191660001916815260200184600019166000191681526020018373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b838110156114015780820151818401526020810190506113e6565b50505050905090810190601f16801561142e5780820380516001836020036101000a031916815260200191505b5095505050505050600060405180830381600087803b15801561145057600080fd5b505af1158015611464573d6000803e3d6000fd5b50505050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16632d658f468f8f8c8c6040518563ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180856000191660001916815260200184600019166000191681526020018060200180602001838103835285818151815260200191508051906020019060200280838360005b8381101561153857808201518184015260208101905061151d565b50505050905001838103825284818151815260200191508051906020019060200280838360005b8381101561157a57808201518184015260208101905061155f565b505050509050019650505050505050600060405180830381600087803b1580156115a357600080fd5b505af11580156115b7573d6000803e3d6000fd5b5050505084806115f35750600073ffffffffffffffffffffffffffffffffffffffff168473ffffffffffffffffffffffffffffffffffffffff16145b1561160b576116068e8e8e8e8e8b614730565b611c18565b600073ffffffffffffffffffffffffffffffffffffffff168473ffffffffffffffffffffffffffffffffffffffff16141515611c175760405180807f66696e616c697a65436f6e73656e73757356657273696f6e286279746573333281526020017f2c627974657333322c616464726573732c6279746573342c62797465732c627981526020017f7465732900000000000000000000000000000000000000000000000000000000815250604401905060405180910390209250828e8e8e8e8e8b60405160240180876000191660001916815260200186600019166000191681526020018573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001847bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19167bffffffffffffffffffffffffffffffffffffffffffffffffffffffff191681526020018060200180602001838103835285818151815260200191508051906020019080838360005b838110156117a557808201518184015260208101905061178a565b50505050905090810190601f1680156117d25780820380516001836020036101000a031916815260200191505b50838103825284818151815260200191508051906020019080838360005b8381101561180b5780820151818401526020810190506117f0565b50505050905090810190601f1680156118385780820380516001836020036101000a031916815260200191505b5098505050505050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff8381831617835250505050915060405180807f61646450726f706f73616c28616464726573732c616464726573732c75696e7481526020017f2c75696e742c6279746573290000000000000000000000000000000000000000815250602c0190506040518091039020338543600086604051602401808673ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018481526020018360ff16815260200180602001828103825283818151815260200191508051906020019080838360005b838110156119ba57808201518184015260208101905061199f565b50505050905090810190601f1680156119e75780820380516001836020036101000a031916815260200191505b509650505050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c285836040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015611b2c578082015181840152602081019050611b11565b50505050905090810190601f168015611b595780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015611b7957600080fd5b505af1158015611b8d573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f820116820180604052506040811015611bb757600080fd5b81019080805190602001909291908051640100000000811115611bd957600080fd5b82810190506020810184811115611bef57600080fd5b8151856001820283011164010000000082111715611c0c57600080fd5b505092919050505050505b5b5050505050505050505050505050565b606080606080846000806000806000611c3f613d7f565b945060405180807f67657456616c696461746f7228616464726573732c627974657333322c61646481526020017f726573732900000000000000000000000000000000000000000000000000000081525060250190506040518091039020935060006001029250600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b158015611d2c57600080fd5b505af1158015611d40573d6000803e3d6000fd5b505050506040513d6020811015611d5657600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152868160440152600080604483895afa84602060903e50506000600102600019168360001916141515611db157600080fd5b611db9613bb2565b995060405180807f61646456616c696461746f722861646472657373290000000000000000000000815250601501905060405180910390208b8b51604051602401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200182815260200192505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509850600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c2611edc61404c565b8b6040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015611f7a578082015181840152602081019050611f5f565b50505050905090810190601f168015611fa75780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015611fc757600080fd5b505af1158015611fdb573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f82011682018060405250604081101561200557600080fd5b8101908080519060200190929190805164010000000081111561202757600080fd5b8281019050602081018481111561203d57600080fd5b815185600182028301116401000000008211171561205a57600080fd5b5050929190505050505060018a51016040519080825280602002602001820160405280156120975781602001602082028038833980820191505090505b5097508997508a888b518151811015156120ad57fe5b9060200190602002019073ffffffffffffffffffffffffffffffffffffffff16908173ffffffffffffffffffffffffffffffffffffffff168152505060405180807f73657450656e64696e6756616c696461746f727328616464726573735b5d2900815250601f0190506040518091039020886040516024018080602001828103825283818151815260200191508051906020019060200280838360005b8381101561216657808201518184015260208101905061214b565b5050505090500192505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509650600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c261221661404c565b896040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b838110156122b4578082015181840152602081019050612299565b50505050905090810190601f1680156122e15780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b15801561230157600080fd5b505af1158015612315573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f82011682018060405250604081101561233f57600080fd5b8101908080519060200190929190805164010000000081111561236157600080fd5b8281019050602081018481111561237757600080fd5b815185600182028301116401000000008211171561239457600080fd5b505092919050505050506123a66141cd565b5050505050505050505050565b600080600080600060405180807f67657450656e64696e6756616c696461746f72436f756e74286164647265737381526020017f2c62797465733332290000000000000000000000000000000000000000000000815250602901905060405180910390209350612421613d7f565b9250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff16141561246857612460612f47565b519450612555565b600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b1580156124ee57600080fd5b505af1158015612502573d6000803e3d6000fd5b505050506040513d602081101561251857600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b600080600080600060405180807f67657446696e616c697a656428616464726573732c6279746573333229000000815250601d019050604051809103902093506125a4613d7f565b9250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff1614156125e457600094506126d1565b600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801561266a57600080fd5b505af115801561267e573d6000803e3d6000fd5b505050506040513d602081101561269457600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b600080600080600060405180807f67657456616c696461746f72436f756e7428616464726573732c62797465733381526020017f3229000000000000000000000000000000000000000000000000000000000000815250602201905060405180910390209350612746613d7f565b9250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff16141561278d57612785612f47565b51945061287a565b600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801561281357600080fd5b505af1158015612827573d6000803e3d6000fd5b505050506040513d602081101561283d57600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b600060608073fffffffffffffffffffffffffffffffffffffffe73ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156128d457600080fd5b6128dc61255c565b1515156128e857600080fd5b6128f061404c565b9250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff1614156129ab577f8564cd629b15f47dc310d45bcbfc9bcf5420b0d51bf0659a16c67f91d2763253612950612f47565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b83811015612993578082015181840152602081019050612978565b505050509050019250505060405180910390a1612f42565b60405180807f66696e616c697a654368616e6765282900000000000000000000000000000000815250601001905060405180910390206129e9613bb2565b6040516024018080602001828103825283818151815260200191508051906020019060200280838360005b83811015612a2f578082015181840152602081019050612a14565b5050505090500192505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509150600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c284846040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015612b76578082015181840152602081019050612b5b565b50505050905090810190601f168015612ba35780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015612bc357600080fd5b505af1158015612bd7573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f820116820180604052506040811015612c0157600080fd5b81019080805190602001909291908051640100000000811115612c2357600080fd5b82810190506020810184811115612c3957600080fd5b8151856001820283011164010000000082111715612c5657600080fd5b5050929190505050505060405180807f66696e616c697a654368616e676528290000000000000000000000000000000081525060100190506040518091039020604051602401604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c284836040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015612dd8578082015181840152602081019050612dbd565b50505050905090810190601f168015612e055780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015612e2557600080fd5b505af1158015612e39573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f820116820180604052506040811015612e6357600080fd5b81019080805190602001909291908051640100000000811115612e8557600080fd5b82810190506020810184811115612e9b57600080fd5b8151856001820283011164010000000082111715612eb857600080fd5b505092919050505050507f8564cd629b15f47dc310d45bcbfc9bcf5420b0d51bf0659a16c67f91d2763253612eeb612f47565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b83811015612f2e578082015181840152602081019050612f13565b505050509050019250505060405180910390a15b505050565b606060008060008060405180807f67657456616c696461746f727328616464726573732c62797465733332290000815250601e01905060405180910390209350612f8f613d7f565b9250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff16141561306e576001604051908082528060200260200182016040528015612ff65781602001602082028038833980820191505090505b5094506000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1685600081518110151561302a57fe5b9060200190602002019073ffffffffffffffffffffffffffffffffffffffff16908173ffffffffffffffffffffffffffffffffffffffff168152505084945061315b565b600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b1580156130f457600080fd5b505af1158015613108573d6000803e3d6000fd5b505050506040513d602081101561311e57600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b6000606061316e61404c565b9150600073ffffffffffffffffffffffffffffffffffffffff168273ffffffffffffffffffffffffffffffffffffffff1614156132625760011515848673ffffffffffffffffffffffffffffffffffffffff167f7cb27b7a2d44ebdb6301eadeb269746c98a49246acca4e8e6d2790a68b70e03f866040518080602001828103825283818151815260200191508051906020019080838360005b83811015613223578082015181840152602081019050613208565b50505050905090810190601f1680156132505780820380516001836020036101000a031916815260200191505b509250505060405180910390a4613636565b60405180807f7265706f727428616464726573732c75696e742c626f6f6c2c62797465732900815250601f01905060405180910390208585600186604051602401808573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018481526020018315151515815260200180602001828103825283818151815260200191508051906020019080838360005b83811015613322578082015181840152602081019050613307565b50505050905090810190601f16801561334f5780820380516001836020036101000a031916815260200191505b5095505050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c283836040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b83811015613493578082015181840152602081019050613478565b50505050905090810190601f1680156134c05780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b1580156134e057600080fd5b505af11580156134f4573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f82011682018060405250604081101561351e57600080fd5b8101908080519060200190929190805164010000000081111561354057600080fd5b8281019050602081018481111561355657600080fd5b815185600182028301116401000000008211171561357357600080fd5b5050929190505050505060011515848673ffffffffffffffffffffffffffffffffffffffff167f7cb27b7a2d44ebdb6301eadeb269746c98a49246acca4e8e6d2790a68b70e03f866040518080602001828103825283818151815260200191508051906020019080838360005b838110156135fb5780820151818401526020810190506135e0565b50505050905090810190601f1680156136285780820380516001836020036101000a031916815260200191505b509250505060405180910390a45b5050505050565b6000606061364961404c565b9150600073ffffffffffffffffffffffffffffffffffffffff168273ffffffffffffffffffffffffffffffffffffffff1614156137715760001515838573ffffffffffffffffffffffffffffffffffffffff167f7cb27b7a2d44ebdb6301eadeb269746c98a49246acca4e8e6d2790a68b70e03f60006040519080825280601f01601f1916602001820160405280156136f15781602001602082028038833980820191505090505b506040518080602001828103825283818151815260200191508051906020019080838360005b83811015613732578082015181840152602081019050613717565b50505050905090810190601f16801561375f5780820380516001836020036101000a031916815260200191505b509250505060405180910390a4613bac565b60405180807f7265706f727428616464726573732c75696e742c626f6f6c2c62797465732900815250601f019050604051809103902084846000806040519080825280601f01601f1916602001820160405280156137de5781602001602082028038833980820191505090505b50604051602401808573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018481526020018315151515815260200180602001828103825283818151815260200191508051906020019080838360005b83811015613864578082015181840152602081019050613849565b50505050905090810190601f1680156138915780820380516001836020036101000a031916815260200191505b5095505050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c283836040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b838110156139d55780820151818401526020810190506139ba565b50505050905090810190601f168015613a025780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b158015613a2257600080fd5b505af1158015613a36573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f820116820180604052506040811015613a6057600080fd5b81019080805190602001909291908051640100000000811115613a8257600080fd5b82810190506020810184811115613a9857600080fd5b8151856001820283011164010000000082111715613ab557600080fd5b5050929190505050505060001515838573ffffffffffffffffffffffffffffffffffffffff167f7cb27b7a2d44ebdb6301eadeb269746c98a49246acca4e8e6d2790a68b70e03f60006040519080825280601f01601f191660200182016040528015613b305781602001602082028038833980820191505090505b506040518080602001828103825283818151815260200191508051906020019080838360005b83811015613b71578082015181840152602081019050613b56565b50505050905090810190601f168015613b9e5780820380516001836020036101000a031916815260200191505b509250505060405180910390a45b50505050565b606060008060008060405180807f67657450656e64696e6756616c696461746f727328616464726573732c62797481526020017f6573333229000000000000000000000000000000000000000000000000000000815250602501905060405180910390209350613c20613d7f565b9250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff161415613c6657613c5f612f47565b9450613d53565b600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b158015613cec57600080fd5b505af1158015613d00573d6000803e3d6000fd5b505050506040513d6020811015613d1657600080fd5b810190808051906020019092919050505091506003549050604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b6000806000806000806060600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b158015613e1057600080fd5b505af1158015613e24573d6000803e3d6000fd5b505050506040513d6020811015613e3a57600080fd5b81019080805190602001909291905050509550600073ffffffffffffffffffffffffffffffffffffffff168673ffffffffffffffffffffffffffffffffffffffff16141515614043573073ffffffffffffffffffffffffffffffffffffffff16600102604051808260001916600019168152602001915050604051809103902094508573ffffffffffffffffffffffffffffffffffffffff166327c422ee600254877f41757261000000000000000000000000000000000000000000000000000000006040518463ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808460001916600019168152602001836000191660001916815260200182600019166000191681526020019350505050600060405180830381600087803b158015613f7557600080fd5b505af1158015613f89573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f8201168201806040525060a0811015613fb357600080fd5b81019080805190602001909291908051906020019092919080519060200190929190805190602001909291908051640100000000811115613ff357600080fd5b8281019050602081018481111561400957600080fd5b815185602082028301116401000000008211171561402657600080fd5b5050929190505050809550819b5082965083975084985050505050505b50505050505090565b600080600080600060405180807f67657456616c696461746f72436f6e736f6c6528616464726573732c6279746581526020017f73333229000000000000000000000000000000000000000000000000000000008152506024019050604051809103902093506140ba613d7f565b9250600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b15801561414257600080fd5b505af1158015614156573d6000803e3d6000fd5b505050506040513d602081101561416c57600080fd5b810190808051906020019092919050505091506003549050600060010260001916816000191614156141a157600094506141c6565b604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b600060606141d961255c565b15156141e457600080fd5b6141ec61404c565b9150600073ffffffffffffffffffffffffffffffffffffffff168273ffffffffffffffffffffffffffffffffffffffff1614156142b0576001430340600019167f55252fa6eee4741b4e24a74a70e9c11fd2c2281df8d6ea13126ff845f7825c89614255613bb2565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b8381101561429857808201518184015260208101905061427d565b505050509050019250505060405180910390a26145ab565b60405180807f73657446696e616c697a656428626f6f6c2900000000000000000000000000008152506012019050604051809103902060006040516024018082151515158152602001915050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663be6002c283836040518363ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200180602001828103825283818151815260200191508051906020019080838360005b8381101561443857808201518184015260208101905061441d565b50505050905090810190601f1680156144655780820380516001836020036101000a031916815260200191505b509350505050600060405180830381600087803b15801561448557600080fd5b505af1158015614499573d6000803e3d6000fd5b505050506040513d6000823e3d601f19601f8201168201806040525060408110156144c357600080fd5b810190808051906020019092919080516401000000008111156144e557600080fd5b828101905060208101848111156144fb57600080fd5b815185600182028301116401000000008211171561451857600080fd5b505092919050505050506001430340600019167f55252fa6eee4741b4e24a74a70e9c11fd2c2281df8d6ea13126ff845f7825c89614554613bb2565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b8381101561459757808201518184015260208101905061457c565b505050509050019250505060405180910390a25b5050565b600080600080600060405180807f676574566f74696e67436f6e736f6c6528616464726573732c6279746573333281526020017f290000000000000000000000000000000000000000000000000000000000000081525060210190506040518091039020935061461d613d7f565b9250600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1663c7f75c556040518163ffffffff167c0100000000000000000000000000000000000000000000000000000000028152600401602060405180830381600087803b1580156146a557600080fd5b505af11580156146b9573d6000803e3d6000fd5b505050506040513d60208110156146cf57600080fd5b810190808051906020019092919050505091506003549050600060010260001916816000191614156147045760009450614729565b604051848152828160040152818160240152600080604483875afa3d6000803e3d6000f35b5050505090565b6000600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1690508073ffffffffffffffffffffffffffffffffffffffff1663ed7870c388888888876040518663ffffffff167c010000000000000000000000000000000000000000000000000000000002815260040180866000191660001916815260200185600019166000191681526020018473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001837bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19167bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1916815260200180602001828103825283818151815260200191508051906020019080838360005b8381101561487557808201518184015260208101905061485a565b50505050905090810190601f1680156148a25780820380516001836020036101000a031916815260200191505b509650505050505050600060405180830381600087803b1580156148c557600080fd5b505af11580156148d9573d6000803e3d6000fd5b505050508073ffffffffffffffffffffffffffffffffffffffff166331511bf0886000866040518463ffffffff167c01000000000000000000000000000000000000000000000000000000000281526004018084600019166000191681526020018315151515815260200180602001828103825283818151815260200191508051906020019080838360005b83811015614980578082015181840152602081019050614965565b50505050905090810190601f1680156149ad5780820380516001836020036101000a031916815260200191505b50945050505050606060405180830381600087803b1580156149ce57600080fd5b505af11580156149e2573d6000803e3d6000fd5b505050506040513d60608110156149f857600080fd5b810190808051906020019092919080519060200190929190805190602001909291905050509091509050600360008291905090600019169055506000600102600019166003546000191614151515614a4f57600080fd5b505050505050505600a165627a7a72305820697718fb0ec7e1e29312efed8fa88404b21575a504d7ec8fd166db11030654770029608060405234801561001057600080fd5b506040516080806139538339810180604052810190808051906020019092919080519060200190929190805190602001909291908051906020019092919050505083838383836000806101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555082600260006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555081600160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff1602179055508060048160001916905550600073ffffffffffffffffffffffffffffffffffffffff166000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614156101b957336000806101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff1602179055505b5050505050505050613783806101d06000396000f300608060405260043610610149576000357c0100000000000000000000000000000000000000000000000000000000900463ffffffff1680630d5777901461014b57806320ac1230146101fa578063251dcc6e146102815780632d658f46146102d857806331511bf01461039d578063323b3c401461047e578063326220bf146105045780633d8ba22a1461054757806345dbac2a146105b05780634bab0a89146105e35780634ff45010146106145780635d8d57a6146106d35780636c5ccc14146107ec5780636d255faf146108635780637418edcf146108ba57806389beb5ad146108eb5780638f1d264f1461092e5780638f283970146109d3578063914bedf414610a16578063a8006dfe14610a47578063be6002c214610a9e578063c50c97d014610b9e578063c6a214ec14610be1578063c7f75c5514610c14578063ed7870c314610c6b575b005b34801561015757600080fd5b5061019a600480360381019080803573ffffffffffffffffffffffffffffffffffffffff1690602001909291908035600019169060200190929190505050610d39565b604051808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200183600019166000191681526020018260001916600019168152602001935050505060405180910390f35b34801561020657600080fd5b50610245600480360381019080803573ffffffffffffffffffffffffffffffffffffffff16906020019092919080359060200190929190505050610d90565b60405180846000191660001916815260200183600019166000191681526020018260001916600019168152602001935050505060405180910390f35b34801561028d57600080fd5b50610296610dd6565b604051808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200191505060405180910390f35b3480156102e457600080fd5b5061039b600480360381019080803560001916906020019092919080356000191690602001909291908035906020019082018035906020019080806020026020016040519081016040528093929190818152602001838360200280828437820191505050505050919291929080359060200190820180359060200190808060200260200160405190810160405280939291908181526020018383602002808284378201915050505050509192919290505050610dfc565b005b3480156103a957600080fd5b5061041e6004803603810190808035600019169060200190929190803515159060200190929190803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290505050611229565b604051808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200183600019166000191681526020018260001916600019168152602001935050505060405180910390f35b34801561048a57600080fd5b506104ad60048036038101908080356000191690602001909291905050506117e5565b6040518080602001828103825283818151815260200191508051906020019060200280838360005b838110156104f05780820151818401526020810190506104d5565b505050509050019250505060405180910390f35b34801561051057600080fd5b50610545600480360381019080803573ffffffffffffffffffffffffffffffffffffffff169060200190929190505050611873565b005b34801561055357600080fd5b50610592600480360381019080803573ffffffffffffffffffffffffffffffffffffffff16906020019092919080359060200190929190505050611912565b60405180826000191660001916815260200191505060405180910390f35b3480156105bc57600080fd5b506105c5611942565b60405180826000191660001916815260200191505060405180910390f35b3480156105ef57600080fd5b506106126004803603810190808035600019169060200190929190505050611948565b005b34801561062057600080fd5b506106b5600480360381019080803573ffffffffffffffffffffffffffffffffffffffff169060200190929190803573ffffffffffffffffffffffffffffffffffffffff169060200190929190803573ffffffffffffffffffffffffffffffffffffffff169060200190929190803573ffffffffffffffffffffffffffffffffffffffff1690602001909291905050506119b1565b60405180826000191660001916815260200191505060405180910390f35b3480156106df57600080fd5b506107026004803603810190808035600019169060200190929190505050611fbe565b604051808673ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200182600019166000191681526020019550505050505060405180910390f35b3480156107f857600080fd5b506108616004803603810190808035600019169060200190929190803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290505050612074565b005b34801561086f57600080fd5b5061087861244e565b604051808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200191505060405180910390f35b3480156108c657600080fd5b506108e96004803603810190808035600019169060200190929190505050612474565b005b3480156108f757600080fd5b5061092c600480360381019080803573ffffffffffffffffffffffffffffffffffffffff1690602001909291905050506127b4565b005b34801561093a57600080fd5b506109d160048036038101908080356000191690602001909291908035600019169060200190929190803573ffffffffffffffffffffffffffffffffffffffff169060200190929190803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290505050612853565b005b3480156109df57600080fd5b50610a14600480360381019080803573ffffffffffffffffffffffffffffffffffffffff169060200190929190505050612cad565b005b348015610a2257600080fd5b50610a456004803603810190808035600019169060200190929190505050612d4b565b005b348015610a5357600080fd5b50610a5c612db4565b604051808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200191505060405180910390f35b610b18600480360381019080803573ffffffffffffffffffffffffffffffffffffffff169060200190929190803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290505050612dd9565b604051808315151515815260200180602001828103825283818151815260200191508051906020019080838360005b83811015610b62578082015181840152602081019050610b47565b50505050905090810190601f168015610b8f5780820380516001836020036101000a031916815260200191505b50935050505060405180910390f35b348015610baa57600080fd5b50610bdf600480360381019080803573ffffffffffffffffffffffffffffffffffffffff16906020019092919050505061317b565b005b348015610bed57600080fd5b50610bf661321a565b60405180826000191660001916815260200191505060405180910390f35b348015610c2057600080fd5b50610c29613220565b604051808273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200191505060405180910390f35b348015610c7757600080fd5b50610d3760048036038101908080356000191690602001909291908035600019169060200190929190803573ffffffffffffffffffffffffffffffffffffffff16906020019092919080357bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19169060200190929190803590602001908201803590602001908080601f0160208091040260200160405190810160405280939291908181526020018383808284378201915050505050509192919290505050613246565b005b6006602052816000526040600020602052806000526040600020600091509150508060000160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff16908060010154908060020154905083565b600860205281600052604060002081815481101515610dab57fe5b9060005260206000209060030201600091509150508060000154908060010154908060020154905083565b600560009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b600080600080600060606000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff16141515610e6157600080fd5b6000600102600019168a6000191614158015610e895750600060010260001916896000191614155b8015610e9757506000885114155b8015610ea557506000875114155b8015610eb2575086518851145b1515610ebd57600080fd5b600073ffffffffffffffffffffffffffffffffffffffff16600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614158015610f2a57506000600102600019166003546000191614155b8015610f4457506000600102600019166004546000191614155b1515610f4f57600080fd5b60405180807f6578656328616464726573732c627974657333322c6279746573290000000000815250601b0190506040518091039020955060405180807f61646446756e6374696f6e7328627974657333322c627974657333322c62797481526020017f6573345b5d2c616464726573735b5d2c62797465732900000000000000000000815250603601905060405180910390209450600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169350600960006003546000191660001916815260200190815260200160002060030160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff161415151561108957600080fd5b60035491506110b56003543373ffffffffffffffffffffffffffffffffffffffff16600102600061361b565b90506004608088516020026020018a51602002602001610148010101036040518781528481600401528381602401526060816044015288516020028a516020020160e46080010181606401528681608401528b81608801528a8160a8015260a08160c80152895160200260c0018160e8015288516020028a516020020160e001816101080152895181610128015260005b8a5160200281101561116f578a8101602001518282016101286020010152806020019050611146565b8951828c51602002016101480152600090505b89516020028110156111b157898101602001518282018c51602002610148016020010152806020019050611182565b60608282018c5160200201610168015283602001518282018c5160200201610168016020015283604001518282018c5160200201610168016040015283606001518282018c51602002016101680160600152600080848460008b5af180151561121957600080fd5b5050505050505050505050505050565b600080600061123661368d565b60006001026000191687600019161415801561125457506000855114155b151561125f57600080fd5b60c06040519081016040528060405180807f676574417070496e6974496e666f28627974657333322c627974657333322c6281526020017f7974657333322900000000000000000000000000000000000000000000000000815250602701905060405180910390207bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1916815260200160405180807f696e6974416e6446696e616c697a6528616464726573732c626f6f6c2c61646481526020017f726573732c62797465732c616464726573735b5d290000000000000000000000815250603501905060405180910390207bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19168152602001600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001600354600019168152602001600454600019168152602001600260009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815250905060405181518152816060015181600401528160800151816024015287816044015260008060648385604001515afa80151561143957600080fd5b60c06000833e816020015195508160400151945081606001518260a0015187151561146357600080fd5b86151561146f57600080fd5b3d840193508851600060208206111561148e5760208106602082010390505b856020015185528560a0015185600401528a856024015282856044015260a085606401528060c0018560840152895160200160648660a4013760a03d0360a0868360c401013e81602002810160e4019050602085828760008d5af193508315156114f757600080fd5b8451965086151561150757600080fd5b505050505081600019163373ffffffffffffffffffffffffffffffffffffffff167f41e90f1c7390824e8e243529aa5ad171738db6bfb0c362d1c7057f8c167c0570868a87604051808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200183600019166000191681526020018260001916600019168152602001935050505060405180910390a36060604051908101604052803373ffffffffffffffffffffffffffffffffffffffff168152602001886000191681526020018460001916815250600660008673ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000206000846000191660001916815260200190815260200160002060008201518160000160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff1602179055506020820151816001019060001916905560408201518160020190600019169055905050600760008573ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001908152602001600020829080600181540180825580915050906001820390600052602060002001600090919290919091509060001916905550600860003373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16815260200190815260200160002060606040519081016040528084600019168152602001896000191681526020018560001916815250908060018154018082558091505090600182039060005260206000209060030201600090919290919091506000820151816000019060001916905560208201518160010190600019169055604082015181600201906000191690555050505093509350939050565b6060600080600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff16915060405180807f67657445786563416c6c6f776564286279746573333229000000000000000000815250601701905060405180910390209050604051818152848160040152600080602483865afa59602001945060203d036020863e50505050919050565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156118ce57600080fd5b80600260006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555050565b60076020528160005260406000208181548110151561192d57fe5b90600052602060002001600091509150505481565b60045481565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156119a357600080fd5b806003816000191690555050565b60008060008060006119c1613734565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff16141515611a1c57600080fd5b600073ffffffffffffffffffffffffffffffffffffffff168a73ffffffffffffffffffffffffffffffffffffffff1614158015611a865750600073ffffffffffffffffffffffffffffffffffffffff168973ffffffffffffffffffffffffffffffffffffffff1614155b8015611abf5750600073ffffffffffffffffffffffffffffffffffffffff168873ffffffffffffffffffffffffffffffffffffffff1614155b8015611af85750600073ffffffffffffffffffffffffffffffffffffffff168773ffffffffffffffffffffffffffffffffffffffff1614155b1515611b0357600080fd5b600073ffffffffffffffffffffffffffffffffffffffff16600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614158015611bb15750600073ffffffffffffffffffffffffffffffffffffffff16600260009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614155b1515611bbc57600080fd5b60405180807f696e6974416e6446696e616c697a6528616464726573732c626f6f6c2c61646481526020017f726573732c62797465732c616464726573735b5d29000000000000000000000081525060350190506040518091039020945060405180807f696e697428290000000000000000000000000000000000000000000000000000815250600601905060405180910390209350600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169250600260009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1691506060604051908101604052808a73ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018973ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018873ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152509050604051858152828160040152600081602401528a816044015260a0816064015260e0816084015260048160a40152848160c4015260038160e4015260005b6060811015611d9c57828101518282610104010152806020019050611d7c565b6020828261010401846000895af1801515611db657600080fd5b82519850505050600060010260001916866000191614151515611dd857600080fd5b856003816000191690555060a0604051908101604052808b73ffffffffffffffffffffffffffffffffffffffff1681526020018a73ffffffffffffffffffffffffffffffffffffffff1681526020018973ffffffffffffffffffffffffffffffffffffffff1681526020018873ffffffffffffffffffffffffffffffffffffffff168152602001876000191681525060096000886000191660001916815260200190815260200160002060008201518160000160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555060208201518160010160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555060408201518160020160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555060608201518160030160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff160217905550608082015181600401906000191690559050505050505050949350505050565b60096020528060005260406000206000915090508060000160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff16908060010160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff16908060020160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff16908060030160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff16908060040154905085565b600080600080600060606000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156120d957600080fd5b6000600102600019168860001916141580156120f757506000875114155b151561210257600080fd5b600073ffffffffffffffffffffffffffffffffffffffff16600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff161415801561216f57506000600102600019166003546000191614155b801561218957506000600102600019166004546000191614155b80156121e45750600073ffffffffffffffffffffffffffffffffffffffff16600260009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614155b15156121ef57600080fd5b60405180807f6578656328616464726573732c627974657333322c6279746573290000000000815250601b0190506040518091039020955060405180807f726567697374657241707028627974657333322c616464726573732c6279746581526020017f732c627974657329000000000000000000000000000000000000000000000000815250602801905060405180910390209450600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169350600960006003546000191660001916815260200190815260200160002060010160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff161415151561232957600080fd5b6003549150612353823373ffffffffffffffffffffffffffffffffffffffff16600102600061361b565b90508651600060208206111561236f5760208106602082010390505b600460808260200161012801010360405188815285816004015284816024015260608160440152826101240181606401528781608401528a8160880152868160a8015260808160c801528260a0018160e80152895181610108015260005b838110156123ef578a81016020015182820161012801528060200190506123cd565b60608282016101280152846020015182820161012801602001528460400151828201610128016040015284606001518282016101280160600152600080848460008c5af180151561243f57600080fd5b50505050505050505050505050565b600260009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b60003373ffffffffffffffffffffffffffffffffffffffff1660066000600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019081526020016000206000846000191660001916815260200190815260200160002060000160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614151561254d57600080fd5b60405180807f6368616e67655363726970744578656328627974657333322c6164647265737381526020017f2900000000000000000000000000000000000000000000000000000000000000815250602101905060405180910390209050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16817c0100000000000000000000000000000000000000000000000000000000900483600560009054906101000a900473ffffffffffffffffffffffffffffffffffffffff166040518363ffffffff167c01000000000000000000000000000000000000000000000000000000000281526004018083600019166000191681526020018273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001925050506000604051808303816000875af19250505015156126b957600080fd5b8160001916600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff167fcf6c41db757e15c5b3f1291c45ff0dd69767c92b5b970a4302ebdf6532ab4b6a600560009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1633604051808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018273ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020019250505060405180910390a35050565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff1614151561280f57600080fd5b80600560006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555050565b60008060008060008060606000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156128b957600080fd5b6000600102600019168b60001916141580156128e157506000600102600019168a6000191614155b80156128ef57506000885114155b15156128fa57600080fd5b600073ffffffffffffffffffffffffffffffffffffffff16600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff161415801561296757506000600102600019166003546000191614155b801561298157506000600102600019166004546000191614155b80156129dc5750600073ffffffffffffffffffffffffffffffffffffffff16600260009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1614155b15156129e757600080fd5b889650600073ffffffffffffffffffffffffffffffffffffffff168773ffffffffffffffffffffffffffffffffffffffff161415612a4557600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1696505b60405180807f6578656328616464726573732c627974657333322c6279746573290000000000815250601b0190506040518091039020955060405180807f726567697374657256657273696f6e28627974657333322c627974657333322c81526020017f616464726573732c62797465732c627974657329000000000000000000000000815250603401905060405180910390209450600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169350600960006003546000191660001916815260200190815260200160002060020160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff1614151515612b7f57600080fd5b6003549150612bab6003543373ffffffffffffffffffffffffffffffffffffffff16600102600061361b565b905087516000602082061115612bc75760208106602082010390505b600460808261016801010360405188815285816004015284816024015260608160440152826101440181606401528781608401528d81608801528c8160a80152898160c8015260a08160e801528260c0018161010801528a5181610128015260005b83811015612c4b578b8101602001518282016101480152806020019050612c29565b60608285016101480152846020015182850161014801602001528460400151828501610148016040015284606001518285016101480160600152600080848460008c5af1801515612c9b57600080fd5b50505050505050505050505050505050565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff16141515612d0857600080fd5b806000806101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555050565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff16141515612da657600080fd5b806004816000191690555050565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b6000606060008060006060612ded8761366c565b8094508195508296505050503373ffffffffffffffffffffffffffffffffffffffff16600102600019168360001916148015612e2857503482145b1515612e3357600080fd5b60405180807f6578656328616464726573732c627974657333322c6279746573290000000000815250601b0190506040518091039020888589604051602401808473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff168152602001836000191660001916815260200180602001828103825283818151815260200191508051906020019080838360005b83811015612eef578082015181840152602081019050612ed4565b50505050905090810190601f168015612f1c5780820380516001836020036101000a031916815260200191505b50945050505050604051602081830303815290604052907bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19166020820180517bffffffffffffffffffffffffffffffffffffffffffffffffffffffff83818316178352505050509050600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff16348260405180828051906020019080838360005b83811015612fea578082015181840152602081019050612fcf565b50505050905090810190601f1680156130175780820380516001836020036101000a031916815260200191505b5091505060006040518083038185875af192505050151561303757600080fd5b5960200194503d85523d6000866020013e60203d1115613062578460200151151561306157600195505b5b8515613112578360001916600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff167f6bde5b03ffd4f222cbcb0ce68937292d6f8f3272ed6f37b0049136b860492f703334604051808373ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff1681526020018281526020019250505060405180910390a35b3373ffffffffffffffffffffffffffffffffffffffff166108fc3073ffffffffffffffffffffffffffffffffffffffff16319081150290604051600060405180830381858888f1935050505015801561316f573d6000803e3d6000fd5b50505050509250929050565b6000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156131d657600080fd5b80600160006101000a81548173ffffffffffffffffffffffffffffffffffffffff021916908373ffffffffffffffffffffffffffffffffffffffff16021790555050565b60035481565b600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1681565b600080600080600060606000809054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff163373ffffffffffffffffffffffffffffffffffffffff161415156132ab57600080fd5b6000600102600019168b60001916141580156132d357506000600102600019168a6000191614155b801561330c5750600073ffffffffffffffffffffffffffffffffffffffff168973ffffffffffffffffffffffffffffffffffffffff1614155b151561331757600080fd5b600073ffffffffffffffffffffffffffffffffffffffff16600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff1673ffffffffffffffffffffffffffffffffffffffff161415801561338457506000600102600019166003546000191614155b801561339e57506000600102600019166004546000191614155b15156133a957600080fd5b60405180807f6578656328616464726573732c627974657333322c6279746573290000000000815250601b0190506040518091039020955060405180807f66696e616c697a6556657273696f6e28627974657333322c627974657333322c81526020017f616464726573732c6279746573342c62797465732c6279746573290000000000815250603b01905060405180910390209450600160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169350600960006003546000191660001916815260200190815260200160002060020160009054906101000a900473ffffffffffffffffffffffffffffffffffffffff169250600073ffffffffffffffffffffffffffffffffffffffff168373ffffffffffffffffffffffffffffffffffffffff16141515156134e357600080fd5b600354915061350f6003543373ffffffffffffffffffffffffffffffffffffffff16600102600061361b565b90508651600060208206111561352b5760208106602082010390505b600460808260200161016801010360405188815285816004015284816024015260608160440152826101640181606401528781608401528d81608801528c8160a801528b8160c801528a8160e8015260c08161010801528260e001816101280152895181610148015260005b838110156135b9578a8101602001518183610168010152806020019050613597565b60608183610168010152846020015181836101680101602001528460400151818361016801016040015284606001518183610168010160600152600080848460008c5af180151561360957600080fd5b50505050505050505050505050505050565b6060806040519080825280601f01601f1916602001820160405280156136505781602001602082028038833980820191505090505b5090508381602001528281604001528181606001529392505050565b60008060008360200151925083604001519150836060015190509193909250565b60c06040519081016040528060007bffffffffffffffffffffffffffffffffffffffffffffffffffffffff1916815260200160007bffffffffffffffffffffffffffffffffffffffffffffffffffffffff19168152602001600073ffffffffffffffffffffffffffffffffffffffff1681526020016000801916815260200160008019168152602001600073ffffffffffffffffffffffffffffffffffffffff1681525090565b6060604051908101604052806003906020820280388339808201915050905050905600a165627a7a723058204518c5bad8bb52040338c8bf4e6cc18e06cf87398511d950effb2b85d003561400290000000000000000000000005a23e5c286e0e825425e0236833535c53d33417e00000000000000000000000000000000000000000000000000000000000000090000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001100000000000000000000000000000000000000000000000000000000000000120000000000000000000000000000000000000000000000000000000000000013000000000000000000000000000000000000000000000000000000000000001400000000000000000000000000000000000000000000000000000000000000150000000000000000000000000000000000000000000000000000000000000000"
                    },
                    "0x5a23e5c286E0E825425E0236833535c53d33417E": {
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
                            "signature": "0x0000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000",
                            "step": "0x0"
                        }
                    }
                },
                "name": "dawn",
                "params": {
                    "chainID": "0x5cc33a0f",
                    "eip140Transition": "0x0",
                    "eip211Transition": "0x0",
                    "eip214Transition": "0x0",
                    "eip658Transition": "0x0",
                    "gasLimitBoundDivisor": "0x400",
                    "maximumExtraDataSize": "0x20",
                    "minGasLimit": "0x1388",
                    "networkID": "0x5cc33a0f"
                }
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
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getMaximumValidatorCount",
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
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getValidatorSupportDivisor",
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
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            }
                        ],
                        "name": "addValidator",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getPendingValidatorCount",
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
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getFinalized",
                        "outputs": [
                            {
                                "name": "",
                                "type": "bool"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "view",
                        "type": "function"
                    },
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getValidatorCount",
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
                    {
                        "constant": false,
                        "inputs": null,
                        "name": "finalizeChange",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getValidators",
                        "outputs": [
                            {
                                "name": "_validators",
                                "type": "address[]"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "view",
                        "type": "function"
                    },
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            },
                            {
                                "name": "_block_number",
                                "type": "uint256"
                            },
                            {
                                "name": "_proof",
                                "type": "bytes"
                            }
                        ],
                        "name": "reportMalicious",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    {
                        "constant": false,
                        "inputs": [
                            {
                                "name": "_validator",
                                "type": "address"
                            },
                            {
                                "name": "_block_number",
                                "type": "uint256"
                            }
                        ],
                        "name": "reportBenign",
                        "outputs": null,
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "function"
                    },
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "getPendingValidators",
                        "outputs": [
                            {
                                "name": "_validators",
                                "type": "address[]"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "view",
                        "type": "function"
                    },
                    {
                        "constant": true,
                        "inputs": null,
                        "name": "masterOfCeremony",
                        "outputs": [
                            {
                                "name": "",
                                "type": "address"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "view",
                        "type": "function"
                    },
                    {
                        "inputs": [
                            {
                                "name": "_master_of_ceremony",
                                "type": "address"
                            },
                            {
                                "name": "_registry_storage",
                                "type": "address"
                            },
                            {
                                "name": "_init_registry",
                                "type": "address"
                            },
                            {
                                "name": "_app_console",
                                "type": "address"
                            },
                            {
                                "name": "_version_console",
                                "type": "address"
                            },
                            {
                                "name": "_impl_console",
                                "type": "address"
                            },
                            {
                                "name": "_consensus_init",
                                "type": "address"
                            },
                            {
                                "name": "_validator_console",
                                "type": "address"
                            },
                            {
                                "name": "_voting_console",
                                "type": "address"
                            }
                        ],
                        "payable": false,
                        "stateMutability": "nonpayable",
                        "type": "constructor"
                    },
                    {
                        "anonymous": false,
                        "inputs": [
                            {
                                "indexed": false,
                                "name": "validators",
                                "type": "address[]"
                            }
                        ],
                        "name": "ChangeFinalized",
                        "type": "event"
                    },
                    {
                        "anonymous": false,
                        "inputs": [
                            {
                                "indexed": true,
                                "name": "parent_hash",
                                "type": "bytes32"
                            },
                            {
                                "indexed": false,
                                "name": "validators",
                                "type": "address[]"
                            }
                        ],
                        "name": "InitiateChange",
                        "type": "event"
                    },
                    {
                        "anonymous": false,
                        "inputs": [
                            {
                                "indexed": true,
                                "name": "registry",
                                "type": "address"
                            },
                            {
                                "indexed": true,
                                "name": "registry_exec_id",
                                "type": "bytes32"
                            }
                        ],
                        "name": "InitializedRegistry",
                        "type": "event"
                    },
                    {
                        "anonymous": false,
                        "inputs": [
                            {
                                "indexed": true,
                                "name": "validator",
                                "type": "address"
                            },
                            {
                                "indexed": true,
                                "name": "block_number",
                                "type": "uint256"
                            },
                            {
                                "indexed": true,
                                "name": "malicious",
                                "type": "bool"
                            },
                            {
                                "indexed": false,
                                "name": "proof",
                                "type": "bytes"
                            }
                        ],
                        "name": "Report",
                        "type": "event"
                    },
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
                            },
                            "ap-south-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ap-southeast-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ap-southeast-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "ca-central-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-central-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "eu-west-3": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "sa-east-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-east-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-east-2": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
                            "us-west-1": {
                                "peer": "providenetwork-node",
                                "validator": "providenetwork-node"
                            },
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
                            "ap-northeast-2": {
                                "peer": {
                                    "0.0.9": "ami-bfa802d1"
                                },
                                "validator": {
                                    "0.0.9": "ami-bfa802d1"
                                }
                            },
                            "ap-south-1": {
                                "peer": {
                                    "0.0.9": "ami-6c2f0703"
                                },
                                "validator": {
                                    "0.0.9": "ami-6c2f0703"
                                }
                            },
                            "ap-southeast-1": {
                                "peer": {
                                    "0.0.9": "ami-578f8a2b"
                                },
                                "validator": {
                                    "0.0.9": "ami-578f8a2b"
                                }
                            },
                            "ap-southeast-2": {
                                "peer": {
                                    "0.0.9": "ami-ed2df18f"
                                },
                                "validator": {
                                    "0.0.9": "ami-ed2df18f"
                                }
                            },
                            "ca-central-1": {
                                "peer": {
                                    "0.0.9": "ami-8d60e3e9"
                                },
                                "validator": {
                                    "0.0.9": "ami-8d60e3e9"
                                }
                            },
                            "eu-central-1": {
                                "peer": {
                                    "0.0.9": "ami-b17c4c5a"
                                },
                                "validator": {
                                    "0.0.9": "ami-b17c4c5a"
                                }
                            },
                            "eu-west-1": {
                                "peer": {
                                    "0.0.9": "ami-86dddbff"
                                },
                                "validator": {
                                    "0.0.9": "ami-86dddbff"
                                }
                            },
                            "eu-west-2": {
                                "peer": {
                                    "0.0.9": "ami-e1799686"
                                },
                                "validator": {
                                    "0.0.9": "ami-e1799686"
                                }
                            },
                            "eu-west-3": {
                                "peer": {
                                    "0.0.9": "ami-132d9c6e"
                                },
                                "validator": {
                                    "0.0.9": "ami-132d9c6e"
                                }
                            },
                            "sa-east-1": {
                                "peer": {
                                    "0.0.9": "ami-67f6ae0b"
                                },
                                "validator": {
                                    "0.0.9": "ami-67f6ae0b"
                                }
                            },
                            "us-east-1": {
                                "peer": {
                                    "0.0.9": "ami-b55a20ca"
                                },
                                "validator": {
                                    "0.0.9": "ami-b55a20ca"
                                }
                            },
                            "us-east-2": {
                                "peer": {
                                    "0.0.9": "ami-c83c02ad"
                                },
                                "validator": {
                                    "0.0.9": "ami-c83c02ad"
                                }
                            },
                            "us-west-1": {
                                "peer": {
                                    "0.0.9": "ami-b95ebbda"
                                },
                                "validator": {
                                    "0.0.9": "ami-b95ebbda"
                                }
                            },
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
            "native_currency": "PRVDTEST",
            "network_id": 1556298255,
            "parity_json_rpc_url": null,
            "protocol_id": "poa"
        },
        "stats": null
    }
]
```

List available peer-to-peer networks and related configuration details.

### Query Parameters

Parameter | Description | Default
--------- | ----------- | -----------
public | flag for displaying public networks | `false`
cloneable | flag for filtering by cloneability of network config | n/a

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