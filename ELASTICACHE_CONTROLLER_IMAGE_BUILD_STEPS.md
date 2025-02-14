# How to build Elasticache ACK Image locally and publish to sites-dev ECR

Create an ECR repository for aws-controllers-k8s in sites-dev. One has been created in a sites-dev ECR private registry via the AWS console:

https://us-east-1.console.aws.amazon.com/ecr/repositories/private/349353150294/aws-controllers-k8s?region=us-east-1

Clone this git repository and from the root directory of the repo, perform these steps:

1. `export SERVICE=elasticache`
1. `sso-credentials`
1. `make build-controller-image`
1. `docker tag aws-controllers-k8s:elasticache-12aba1c-dirty 349353150294.dkr.ecr.us-east-1.amazonaws.com/aws-controllers-k8s:latest`
1. `docker push 349353150294.dkr.ecr.us-east-1.amazonaws.com/aws-controllers-k8s:latest`

