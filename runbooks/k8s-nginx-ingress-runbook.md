<!--
    Written in the format prescribed by https://github.com/Financial-Times/runbook.md.
    Any future edits should abide by this format.
-->
# UPP Kubernetes NGINX Ingress

A helm deployment package for a simple NGINX ingress service via an AWS ELB.

## Code

k8s-nginx-ingress

## Primary URL

https://github.com/Financial-Times/k8s-nginx-ingress

## Service Tier

Platinum

## Lifecycle Stage

Production

## Host Platform

AWS

## Architecture

An Ingress Controller is a daemon, deployed as a Kubernetes pod, that watches the apiservers's /ingresses endpoint for updates to the Ingress resource. Its job is to satisfy requests for Ingresses.
There are routing stacks in PAC, Publish and Delivery clusters that use NGINX Ingress Controllers from Kubernetes.

## Contains Personal Data

No

## Contains Sensitive Data

No

<!-- Placeholder - remove HTML comment markers to activate
## Can Download Personal Data
Choose Yes or No

...or delete this placeholder if not applicable to this system
-->

<!-- Placeholder - remove HTML comment markers to activate
## Can Contact Individuals
Choose Yes or No

...or delete this placeholder if not applicable to this system
-->

## Failover Architecture Type

ActiveActive

## Failover Process Type

PartiallyAutomated

## Failback Process Type

PartiallyAutomated

## Failover Details

The service is deployed in all (PAC, Publish and Delivery) clusters. The failover guides for all clusters are located here: <https://github.com/Financial-Times/upp-docs/tree/master/failover-guides>

## Data Recovery Process Type

None

<!-- Placeholder - remove HTML comment markers to activate
## Data Recovery Details
Enter descriptive text satisfying the following:
The actions required to restore the data for this system. Either provide a set of numbered steps or a link to a detailed process that operations can follow.

...or delete this placeholder if not applicable to this system
-->

## Release Process Type

PartiallyAutomated

## Rollback Process Type

Manual

## Release Details

The release is triggered by making a Github release which is then picked up by a Jenkins multibranch pipeline. The Jenkins pipeline should be manually started in order for it to deploy the helm package to the Kubernetes clusters.

<!-- Placeholder - remove HTML comment markers to activate
## Heroku Pipeline Name
Enter descriptive text satisfying the following:
This is the name of the Heroku pipeline for this system. If you don't have a pipeline, this is the name of the app in Heroku. A pipeline is a group of Heroku apps that share the same codebase where each app in a pipeline represents the different stages in a continuous delivery workflow, i.e. staging, production.

...or delete this placeholder if not applicable to this system
-->

## Key Management Process Type

None

## Key Management Details

There is no key rotation procedure for this system.

## Monitoring

*   <https://pac-prod-eu.upp.ft.com/__health>
*   <https://pac-prod-us.upp.ft.com/__health>
*   <https://upp-prod-publish-eu.upp.ft.com/__health>
*   <https://upp-prod-publish-us.upp.ft.com/__health>
*   <https://upp-prod-delivery-us.upp.ft.com/__health>
*   <https://upp-prod-delivery-eu.upp.ft.com/__health>

## First Line Troubleshooting

Please refer to <https://github.com/Financial-Times/upp-docs/tree/master/guides/ops/first-line-troubleshooting>

## Second Line Troubleshooting

There is no need for any second line troubleshooting.