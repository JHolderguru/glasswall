### The pipeline is a full CI/CD serverless pipeline for building and deploying the API. In this pseudocode I will be referencing CloudFormation to create the pipeline, all resources, and any permissions needed.

### The following resources are the Prerequisites:

### An S3 bucket to store deployment artifacts.
### AWS CodeBuild stage to build any changes checked into the repo.
### The AWS CodePipeline (yaml file) API that will watch for changes on your repo, and push these changes through to build and deployment steps.
### All IAM roles and policies required.
### Github repo


### 1. On AWS (Create stack)Name the project and Click next (fill in the parameters as desired).
### 2. Go to github.com/settings/tokens generate a personal access token.
### 3. Add your Token to AWS repo hook then click create.
### 4. The Pipeline will then be built and you the stack will be created on the CloudFormation Screen.
### 5.On the Codepipeline  we can see the completed pipeline,
### 6.it will look for the latest commit of the code in the github repo and run the build steps that were defined in our container i.e nodejs (which has npm to pull out the packages).
### 8.Click on the build step to see the logs.
### 9. Once that is complete it will proceed to the Deploy stage.
### 10. Click on Amazon API Gateway click resources and click get pro and there should a live URL.
