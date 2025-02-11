# CloudFormation

## What is AWS CloudFormation?

AWS CloudFormation is a service that helps you model and set up your AWS resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and CloudFormation takes care of provisioning and configuring those resources for you. You don't need to individually create and configure AWS resources and figure out what's dependent on what; CloudFormation handles that. The following scenarios demonstrate how CloudFormation can help.


## Steps to Create a CloudFormation Template
### Create a CloudFormation Template:
You can write a CloudFormation template in either YAML or JSON format. The template describes the AWS resources you want to create and their properties.

## Steps to Create a CloudFormation Stack
Once your template is ready, follow these steps to create a stack in AWS:

### Method 1: Using AWS Management Console
Open the CloudFormation Console:

Log in to the AWS Management Console.
Go to the CloudFormation service (you can search for it in the search bar).
### Create a Stack:

Click on Create stack in the CloudFormation dashboard.
Choose With new resources (standard).
Specify Template:

### Choose a template: 
You can upload your template directly from your local machine by selecting Upload a template file. Browse and select the file you created earlier (ec2-instance.yaml).
Alternatively, you can choose Amazon S3 URL if you’ve uploaded your template to an S3 bucket.
Specify Stack Details:

### Stack name: 
Provide a name for your stack, like MyEC2Stack.
Parameters (Optional): If your template has parameters (e.g., AMI ID, instance type), fill them in.
Configure Stack Options:

Optionally, you can configure advanced options such as permissions, stack policies, and tags.
Once you're done, click Next.
### Review and Create:

Review the settings you’ve configured.
If everything looks good, click Create stack.
### Monitor Stack Creation:

CloudFormation will start creating resources as per the template. You can monitor the progress from the Events tab in the stack’s detail page.
