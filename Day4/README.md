## Code Build

1. Log in to the CodeBuild console.
2. Create a new CodeBuild project.
3. Enter a name for your project.
4. Add your source code. In my case, I used my personal GitHub repository.
5. Configure your GitHub personal access token with CodeBuild.
6. Obtain your personal access token from GitHub:
Log in to your GitHub account.
Go to Settings.
Click on Developer settings, then select Personal access tokens (classic).
Generate a new token and update it in Secrets Manager.
7. Choose primary source webhook events:
8. Single Build (Trigger a single build).
9. Choose your environment:
Select AWS managed image environments (Ubuntu or Amazon Linux).
10. Create a buildspec.yml file and add it to CodeBuild or store it in your S3 bucket.
11. Create a service role with the necessary permissions. Your CodeBuild project should be able to communicate with the System Manager to get parameters from the Parameter Store that are used in your buildspec.yml.
12. Start the build and verify the logs.
