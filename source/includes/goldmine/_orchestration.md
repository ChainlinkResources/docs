# Orchestration

Provide supports orchestration of load balanced peer-to-peer networks across multiple regions and data centers using the [network](/microservices/goldmine#networks) and [node](/microservices/goldmine#node) APIs.

## Amazon Web Services

<img class="cloud-provider" alt="Amazon Web Services" src="https://s3.amazonaws.com/static.provide.services/img/aws-light.png" />

<pre><b>target</b>&nbsp;aws</pre>

### Credentials

The following object illustrates how to securely pass your IAM `credentials` within a `config`.

Name | Description
--------- | -------- |
aws_access_key_id | the AWS access key id
aws_secret_access_key | the AWS secret access key

### VPC Considerations

<i>Documentation forthcoming.</i>

### Load Balancing

Provide leverages the second-generation Elastic Load Balancing (ELB) service on your behalf when you deploy network nodes. Currently the platform orchestrates the provisioning for you implicitly when you attempt to deploy your first node for a unique network and region. We support orchestration in all AWS availability zones.

When a load balancer is provisioned for you by the platform, it is currently added to a list of regional load balancers under management which are, in turn, used in a pool-like fashion (i.e., a simple round-robin algorithm is used to distribute JSON-RPC and similar requests across all healthy balancers in a region). We are considering other algorithms for distributing this load.

## Microsoft Azure

<img class="cloud-provider" alt="Microsoft Azure" src="https://s3.amazonaws.com/static.provide.services/img/azure-light.png" />

<pre><b>target</b>&nbsp;azure</pre>

### Credentials

The following object illustrates how to securely pass your Azure API `credentials` within a `config`.

Name | Description
--------- | -------- |
azure_tenant_id | the Azure directory (tenant) id
azure_client_id | the Azure application (client) id
azure_client_secret | the Azure client secret

<i>Documentation forthcoming.</i>

## Docker

<img class="cloud-provider" alt="Docker" src="https://s3.amazonaws.com/static.provide.services/img/docker-light.png" />

<pre><b>target</b>&nbsp;docker</pre>

<i>Documentation forthcoming.</i>

## On-Premise Support

<i>Documentation forthcoming.</i>
