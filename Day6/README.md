# CodeDeploy

## Prerequisites:

1. Create an EC2 instance and configure the necessary security group rules (e.g., allow port 22 for SSH, allow all sources (0.0.0.0/0)).

2. Create a tag for your EC2 instance and modify the tags as needed.

3. Install Docker to run your application.

4. Follow the installation steps from the official Docker documentation.

5. Install the CodeDeploy Agent. Follow the official AWS documentation for installing the CodeDeploy agent.

6. Create a role for your EC2 instance to allow it to communicate with CodeDeploy and assign the role to your instance.

7. Place your appspec.yml file in the root of your Git repository, and ensure your script files are in the same directory.

## What is the CodeDeploy Agent?

The AWS CodeDeploy Agent is a software component that helps AWS CodeDeploy perform deployment operations on your instances. It runs on EC2 instances or on-premises servers, ensuring that the deployment package is installed, configured, and updated correctly. The agent interacts with the AWS CodeDeploy service to carry out the deployment process by following the instructions specified in the deployment configuration.

## CodeDeploy Setup:
1. Login to the CodeDeploy console in AWS.

2. Create an application and enter the application name.

3. Choose the compute platform (e.g., EC2/On-Premises, Lambda). In my case, I have chosen EC2/On-Premises.

4. Add a tag.

Note: Get tags from your EC2 instance to identify the EC2 instance for deploying your application.
Steps:

5. Go to the EC2 instance console.
Click on your EC2 instance.
Click on Actions > Instance Settings > Manage Tags.
Create a Deployment Group.

6. Create a role that grants permission for CodeDeploy to communicate with your EC2 instance.

7 Choose the deployment type. In my case, I have chosen "In-place".

8. Environment Configuration: Choose tags for the EC2 instance. The CodeDeploy group uses tags to identify the EC2 instance.

9. Create a deployment once the deployment group is created.

10. Choose the revision type. In my case, I have chosen "My application store on GitHub".

11. Define the GitHub repository name and commit ID to check CodeDeploy for testing.

Example:

Repository: Gowthams1999-commits/aws-devops-project-gowtham
Get the latest commit ID from GitHub and paste it in the commit ID field.

12. Create the deployment and verify the application on your EC2 instance.

13. Integrate your CodeDeploy setup with CodePipeline to complete your end-to-end CI/CD process in AWS.


