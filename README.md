# ecs-service-connect
Enable service-to-service communication using ECS Service connect. 

This cloudformation deploys VPC with 2 public subnets, internet facing ALB, creates two ECS Clusters, ECS task definition and services with Fargate as a launch type for all application components in the public subnets, and adds the UI service as a target to the ALB and outputs the DNS name.

```bash
aws cloudformation create-stack --stack-name ecs-service-connect --template-body file://ecs-service-connect.yaml --capabilities CAPABILITY_NAMED_IAM
```
