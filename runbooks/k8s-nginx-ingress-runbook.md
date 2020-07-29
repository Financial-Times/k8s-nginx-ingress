# UPP Kubernetes NGINX Ingress

A helm deployment package for a simple NGINX ingress service via an AWS ELB.

## Primary URL

<https://github.com/Financial-Times/k8s-nginx-ingress>

## Service Tier

Platinum

## Lifecycle Stage

Production

## Delivered By

content

## Supported By

content

## Known About By

- donislav.belev
- mihail.mihaylov
- boyko.boykov
- dimitar.terziev
- miroslav.gatsanoga
- kalin.arsov

## Host Platform

AWS

## Architecture

An Ingress Controller is a daemon, deployed as a Kubernetes pod, that watches the apiservers's /ingresses endpoint for updates to the Ingress resource. Its job is to satisfy requests for Ingresses.
There are routing stacks in PAC, Publish and Delivery clusters that use NGINX Ingress Controllers from Kubernetes.

## Contains Personal Data

No

## Contains Sensitive Data

No

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

## Release Process Type

PartiallyAutomated

## Rollback Process Type

Manual

## Release Details

The release is triggered by making a Github release which is then picked up by a Jenkins multibranch pipeline. The Jenkins pipeline should be manually started in order for it to deploy the helm package to the Kubernetes clusters.

## Key Management Process Type

None

## Key Management Details

There is no key rotation procedure for this system.

## Monitoring

- https://pac-prod-eu.upp.ft.com/__health
- https://pac-prod-us.upp.ft.com/__health
- https://upp-prod-publish-eu.upp.ft.com/__health
- https://upp-prod-publish-us.upp.ft.com/__health
- https://upp-prod-delivery-us.upp.ft.com/__health
- https://upp-prod-delivery-eu.upp.ft.com/__health

## First Line Troubleshooting

Please refer to <https://github.com/Financial-Times/upp-docs/tree/master/guides/ops/first-line-troubleshooting>

## Second Line Troubleshooting

There is no need for any second line troubleshooting.
