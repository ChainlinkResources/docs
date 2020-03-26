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

### AWS Policy & Role Configuration

A prerequisite to using AWS as an orchestration `target` with Provide is creating a policy and attaching it to a role using the *Identity Access Manager (IAM)* service. A sample policy definition has been provided; you can modify the policy JSON to be more restrictive based on the needs of your organization.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "acm:*"
      ],
      "Resource": "*"
    },
    {
      "Action": "ec2:*",
      "Effect": "Allow",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "elasticloadbalancing:*",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "cloudwatch:*",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "autoscaling:*",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "iam:CreateServiceLinkedRole",
      "Resource": "*",
      "Condition": {
        "StringEquals": {
          "iam:AWSServiceName": [
            "autoscaling.amazonaws.com",
            "ec2scheduled.amazonaws.com",
            "elasticloadbalancing.amazonaws.com",
            "spot.amazonaws.com",
            "spotfleet.amazonaws.com",
            "transitgateway.amazonaws.com"
          ]
        }
      }
    },
    {
      "Action": [
        "logs:Describe*",
        "logs:Get*",
        "logs:List*",
        "logs:StartQuery",
        "logs:StopQuery",
        "logs:TestMetricFilter",
        "logs:FilterLogEvents"
      ],
      "Effect": "Allow",
      "Resource": "*"
    }
  ]
}
```


### VPC Considerations

<i>Documentation forthcoming.</i>

### Load Balancing

Provide leverages the second-generation Elastic Load Balancing (ELB) service on your behalf when you deploy network nodes. Currently the platform orchestrates the provisioning for you implicitly when you attempt to deploy your first node for a unique network and region. We support orchestration in all AWS availability zones.

When a load balancer is provisioned for you by the platform, it is currently added to a list of regional load balancers under management which are, in turn, used in a pool-like fashion (i.e., a simple round-robin algorithm is used to distribute JSON-RPC and similar requests across all healthy balancers in a region). We are considering other algorithms for distributing this load.

## Microsoft Azure

<img class="cloud-provider" alt="Microsoft Azure" src="https://s3.amazonaws.com/static.provide.services/img/azure-light.png" />

<pre><b>target</b>&nbsp;azure</pre>

### Azure Application & Subscription-Scoped RBAC

A prerequisite to using Azure as an orchestration `target` with Provide is registering a directory application and assigning the appropriate permissions via a custom role. This role should be created using the *Access control (IAM)* tool located within the *Azure Subscriptions* service. A sample role definition has been provided; you will need to update the `assignableScopes` section provided in the sample JSON with your subscription scope.

```json
{
  "properties": {
    "roleName": "Provide Azure Role",
    "description": "permissions granted to Azure applications for use with Provide",
    "assignableScopes": [
      "/subscriptions/14e122a1-1a51-4ffa-b956-985f3e855394"
    ],
    "permissions": [
      {
        "actions": [
          "Microsoft.Authorization/*/read",
          "Microsoft.Insights/alertRules/*",
          "Microsoft.Network/*",
          "Microsoft.ResourceHealth/availabilityStatuses/read",
          "Microsoft.Resources/deployments/*",
          "Microsoft.Resources/subscriptions/resourceGroups/*",
          "Microsoft.Support/*"
        ],
        "notActions": [],
        "dataActions": [],
        "notDataActions": []
      }
    ]
  }
}
```

Register a new single-tenant application within the *Azure Active Directory* service, create a custom role (as describe above) and assign the role to the registered application.

### Credentials

The following object illustrates how to securely pass your Azure API `credentials` within a `config`.

Name | Description
--------- | -------- |
azure_subscription_id | the Azure subscription id
azure_tenant_id | the Azure directory tenant id
azure_client_id | the Azure application client id
azure_client_secret | the Azure client secret


## Docker

<img class="cloud-provider" alt="Docker" src="https://s3.amazonaws.com/static.provide.services/img/docker-light.png" />

<pre><b>target</b>&nbsp;docker</pre>

<i>Documentation forthcoming.</i>

## On-Premise Support

<i>Documentation forthcoming.</i>
