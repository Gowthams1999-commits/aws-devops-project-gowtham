# Create an EKS Cluster Using the Fargate Method

## What is AWS Fargate in EKS?
In Amazon Elastic Kubernetes Service (EKS), AWS Fargate provides a serverless compute engine for running Kubernetes pods. With Fargate, you don't need to provision or manage EC2 instances to run your Kubernetes workloads. It automatically manages the infrastructure for you, scaling based on the needs of your containers.

## Create EKS Cluster with Fargate:
You can create a cluster with the eksctl command. Here's how to do it:



eksctl create cluster --name my-cluster --region <region-code> --fargate

* Replace <region-code> with the AWS region where you want to create your cluster.
* Replace my-cluster with your desired cluster name.

For example:



eksctl create cluster --name simple-app-cluster --region us-east-1 --fargate

## View Kubernetes Resources:
To check the nodes running in your cluster:



kubectl get nodes -o wide

## To view the workloads running on your cluster:



kubectl get pods -A -o wide

## Delete Your Cluster:
If you want to delete your cluster, use the following command:



eksctl delete cluster --name my-cluster --region <region-code>

## Deploy a Sample Application to Your Cluster
To deploy an application on Fargate, you must first ensure you have an existing Fargate profile that includes the namespace for your application.

## Create Fargate Profile:



eksctl create fargateprofile \
    --cluster my-cluster \
    --name my-fargate-profile \
    --namespace my-kubernetes-namespace \
    --labels key=value

## Create Application Load Balancer (ALB) Controller Using Helm:

* Create an OIDC provider before setting up the ALB controller.
* Download the necessary policy, attach the policy to the role, and associate the role with your EKS cluster.
* Install Application Load Balancer (ALB) Using Helm.

* Create Kubernetes Resources:

* Create Deployment, Pods, Services, and Ingress resources for your application.
* Expose Your Application to the External World Using Ingress:

* Use the Ingress resource to expose your application externally, allowing it to be accessed from the internet.

## Additional Notes:
Ensure that your EKS cluster is properly configured with the necessary IAM roles and permissions to allow these operations.
You can adjust the configurations of Fargate, Helm, and Kubernetes resources based on your application's needs.
