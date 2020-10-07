# What the Hack: DevOps with GitHub 

## Challenge 5 – Continuous Delivery
[< Previous](challenge04.md) - [Home](../readme.md) - [Next >](challenge06.md)

### Introduction

In DevOps after we automate our build process, we want to automate our release process, we do this with a technique called Continuous Delivery. Please take a moment to review this brief article talking about why this is important. 

1. [What is Continuous Delivery?](https://docs.microsoft.com/en-us/azure/devops/learn/what-is-continuous-delivery)

### Challenge

In this challenge, we will use GitHub Actions to deploy our container image to the dev, test, and prod environments. Extend the workflow you created in Challenge #4 to:

1. Configure your `dev` environment to pull the latest container image from ACR. 
   - Login to Azure, if needed
   - Use the `Azure/webapps-deploy@v2` action to update the Web App to pull the latest image from ACR. Key parameters to configure:
      - `app-name`
      - `images` (i.e., `<prefix>devopsreg`.azurecr.io/`<prefix>devopsimage`:`${{ GITHUB_RUN_NUMBER }}`)
2. Make a small change to your application  (i.e.,`/Application/aspnet-core-dotnet-core/Views/Home/Index.cshtml`), commit, push, monitor the workflow and see if the change shows up on the dev instance of the website.

**NOTE**: Normally, we would have you configure phased releases using manual approvals next, but as of 10/7/20, GitHub doesn't have a way of implementing manual approvals - which would require manual approval *before* deploying to test and prod respectively. It is on the [GitHub roadmap](https://github.com/github/roadmap/issues/99), due to be available by the end of 2020.

### Success Criteria

1. A small change to your application shows up on the website running in the dev environment (i.e., `<prefix>devops-dev`.azurewebsites.net).

[< Previous](challenge04.md) - [Home](../readme.md) - [Next >](challenge06.md)