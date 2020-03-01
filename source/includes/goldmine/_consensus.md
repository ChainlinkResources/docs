# Protocol Support

Provide is a modular integration fabric standardizing on support for a subset of the peer-to-peer platforms and protocols being maintained [in this repository](https://github.com/providenetwork/dockerfiles) in partnership with [whiteblock](https://whiteblock.io).

<br/>
<img class="protocol-provider" alt="EVM" src="https://s3.amazonaws.com/static.provide.services/img/evm-logo.png" />
<img class="protocol-provider" alt="Parity" src="https://s3.amazonaws.com/static.provide.services/img/parity-light.png" />
<img class="protocol-provider" alt="Handshake" src="https://s3.amazonaws.com/static.provide.services/img/quorum-light.png" />
<img class="protocol-provider" alt="Hyperledger" src="https://s3.amazonaws.com/static.provide.services/img/hyperledger-light.png" />
<img class="protocol-provider" alt="Bitcoin" src="https://s3.amazonaws.com/static.provide.services/img/bcoin-light.png" />
<img class="protocol-provider" alt="Handshake" src="https://s3.amazonaws.com/static.provide.services/img/handshake-light.png" />
<img class="protocol-provider" alt="whiteblock" style="height: 36px; margin: 0px 0px 5px 90px;" src="https://s3.amazonaws.com/static.provide.services/img/whiteblock-black.png" />

### Genesis/Pluggable Consensus

A `Network` can be configured from scratch using [this API](/microservices/goldmine#create-a-network). Depending on which platform is chosen, pluggable consensus may be supported. Additional documentation detailing how to leverage [supported platforms and protocols](https://github.com/providenetwork/dockerfiles) as well as specific genesis parameterization for each will be released in the near future.
