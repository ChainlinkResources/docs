# Protocol Support

The Provide Platform is a scalable, protocol-agnostic PaaS for deploying public, private or permissioned blockchain networks. Our supported networks, protocols and projects are outlined below as well as in the [provide.network node](https://github.com/providenetwork/node) repository.

## Consensus

Provide supports various configurable consensus protocols depending on the peer-to-peer network configuration of a given network (see Supported Peer-to-Peer Clients below).
Additional consensus discussion & considerations forthcoming.

## Peer-to-Peer Clients

<img alt="Peer-to-Peer Clients Supported on Provide Platform" src="https://s3.amazonaws.com/static.provide.services/img/supported-p2p-clients.png" />

### EVM

The Ethereum virtual machine was our go-to-market platform and was chosen due to its popularity among the open source community.

We support various clients for the EVM, including Geth and Parity, Quorum (select consensus mechanisms) and ewasm (experimental). 

### Bcoin

The node.js implementation of the Bitcoin protocol.

### Handshake

Handshake is a UTXO-based blockchain protocol which manages the registration, renewal and transfer of DNS top-level domains (TLDs).

### Hyperledger

We are supporting Hyperledger Burrow with Tendermint consensus as well as Hyperledger Fabric.
