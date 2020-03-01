# Orchestration

<img class="cloud-provider" alt="Amazon Web Services" src="https://s3.amazonaws.com/static.provide.services/img/aws-light.png" />
<img class="cloud-provider" alt="Microsoft Azure" src="https://s3.amazonaws.com/static.provide.services/img/azure-light.png" />
<img class="cloud-provider" alt="Docker" src="https://s3.amazonaws.com/static.provide.services/img/docker-light.png" />

<i>Documentation forthcoming.</i>

## Amazon Web Services

<i>Documentation forthcoming.</i>

### Your AWS Credentials (IAM)

<i>Documentation forthcoming.</i>

### VPC Considerations

<i>Documentation forthcoming.</i>

### Security

<i>Documentation forthcoming.</i>

### Load Balancing

Provide leverages the second-generation Elastic Load Balancing (ELB) service on your behalf when you deploy network nodes. Currently the platform orchestrates the provisioning for you implicitly when you attempt to deploy your first node for a unique network and region. We support orchestration in all AWS availability zones.

When a load balancer is provisioned for you by the platform, it is currently added to a list of regional load balancers under management which are, in turn, used in a pool-like fashion (i.e., a simple round-robin algorithm is used to distribute JSON-RPC and similar requests across all healthy balancers in a region). We are considering other algorithms for distributing this load.

### Elastic Container Service (ECS & Fargate)

<i>Documentation forthcoming.</i>


## Microsoft Azure

<i>Documentation forthcoming.</i>


## Google Cloud Platform

<i>Documentation forthcoming.</i>


## Docker

<i>Documentation forthcoming.</i>


## Kubernetes

<i>Documentation forthcoming.</i>


## On-Premise Support

<i>Documentation forthcoming.</i>
