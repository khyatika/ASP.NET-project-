Pipeline-7: Deploying a asp.net application with SonarQube to azure app service using Azure DevOps
Steps:
Navigate to Azure DevOps and create a new project named pipeline-7
Navigate to repos
Click on Import and import this repo https://github.com/luckysuie/web-asp-dontnet
Open sonarcloud.io and login into your account using GitHub
Create a organization and create a project named dotnetanalysis in that organization
Navigate to my account--> security-->Generate Token Note down the below
project name
project key
Token
Navigate to Azure DevOps and move project settings and create a service connection for sonar cloud
search SonarQube and provide the necessary details
you should see you connection successful
Navigate to portal and create azure app service
select webapp
Enter the name
Runtime Stack: .NET 8(LTS)
Operating system : windows
Region: Canada central
Navigate to pipelines and start writing the pipeline for
CI Continuous Integration
Install NuGet
Restore packages
Prepare SonarCloud
Build the project
Run SonarCloud Analysis
Publish SonarCloud Results
Publish Web App
Publish Build Artifact
CD Continuous Deployment
Download the artifact
Deploy to Azure app service
