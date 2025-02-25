
## What is ECR?

Amazon Elastic Container Registry (ECR) is a fully managed service in AWS that enables you to store, manage, and deploy Docker images securely. It integrates with other AWS services such as Elastic Kubernetes Service (EKS) and ECS (Elastic Container Service).

## Prerequestics:

 * Install Docker 

 * Install AWS CLI and Configure AWS CLI

  
 * Create a Repository using AWS CLI

Example:

aws ecr create-repository \
     --repository-name hello-repository \
     --region us-east-1


## Get Started ECR

1. Create a Docker file


2. Build Docker images

docker build --network host -t "hello-world:latest" .

3. Authenticate to ECR repo

aws ecr get-login-password --region region | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com

Note: Chage region and aws-account-id

4. Push Docker images to ECR

* List Docker image

docker images

* Tag Docker image

docker tag hello-world:latest aws_account_id.dkr.ecr.region.amazonaws.com/hello-repository


5. Push Docker images


docker push aws_account_id.dkr.ecr.region.amazonaws.com/hello-repository

8. Pull images

docker pull aws_account_id.dkr.ecr.region.amazonaws.com/hello-repository

9. Run container using ECR image

docker build -it -d --name=<container-name> -p <localhost-port>:<application/container-port> image





