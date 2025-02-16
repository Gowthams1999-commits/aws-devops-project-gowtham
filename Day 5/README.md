# Code Pipeline

1. Login to CodePipeline Console.

2. Create a Pipeline and give it a name.

3. Choose the pipeline type (In my case, I chose Pipeline V2 as required).

4. In the Source section, configure the following fields:

* Action Provider: GitHub (via GitHub App)
* Connection: Click on "Connect to GitHub" and create a connection to your GitHub account.
* Repository Name: Your repo name should be in the following format:
* Example: Gowthams1999-commits/aws-devops-project-gowtham
* Branch Name: Select the branch you want to use (in my case, the branch name is master).

5. In the Build section, configure the following:

* Action Name: Build
* Action Provider: AWS CodeBuild
* Region: Choose the required region.
* Input Artifact: SourceArtifact
* Project Name: Choose your CodeBuild project name.
* Build Type: Single Build
* Output Artifact: BuildArtifact
