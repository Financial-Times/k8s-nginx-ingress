# Kubernetes NGINX Ingress

A helm deployment package for a simple NGINX ingress service via an AWS ELB.

## Usage

First create an `override.yaml` file which contains the AWS ARN for the SSL certificate you wish the ELB to use.

```
# override.yaml

service:
  ssl:
    aws_certificate_arn: "arn:aws:example-arn"
```

Next check the `helm/k8s-nginx-ingress/app-configs` directory for a suitable configuration for your requirements, or create a new one.

To deploy to the configured kubernetes cluster, run:

```
helm upgrade -i nginx-ingress ./helm/k8s-nginx-ingress -f ./helm/k8s-nginx-ingress/app-configs/nginx-ingress_pac.yaml -f override.yaml
```
