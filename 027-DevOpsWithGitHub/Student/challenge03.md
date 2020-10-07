# What the Hack: DevOps with GitHub 

## Challenge 3 - Infrastructure as Code (IaC)
[< Previous](challenge02.md) - [Home](../readme.md) - [Next >](challenge04.md)

### Introduction

Now that we have some code, we need an environment to deploy it to! The term Infrastructure as Code (IaC) refers to using templates (code) to repeatedly and consistently create the dev, test, prod (infrastructure) environments. We can automate the process of deploying the Azure services we need with an Azure Resource Manager (ARM) template. 

Review the following articles:

- [Azure Resource Manager overview](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview)
- [Create Azure Resource Manager template](https://docs.microsoft.com/en-us/azure/azure-resource-manager/how-to-create-template)


### Challenge

We will use GitHub Actions to automate the deployment of our Azure infrastructure. For our application, we will deploy 3 environments: `dev`, `test` and `prod`. Each environment will have its own Web App, however all of our environments will share a single Resource Group, App Service Plan, Application Insights instance, and Azure Container Registry. NOTE: in real deployments, you will likely not share all of these resources.

First, we are going to deploy the dev environment:

1. Review the [ARM template](./Code/ARM-Templates/container-webapp-template.json). Notice how it defines a number of parameters and uses them to create the Resource Group, App Service Plan, Web App, Application Insights, and Azure Container Registry.
2. Update the ARM template, replacing the `<prefix>` part with a unique lowercase 5 letter name.
3. Create a GitHub workflow (`deployDev.yml`) that accomplishes the following ([hint](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-github-actions)):
    - Only runs when changes are made to the workflow file itself or the ARM template in your repo ([hint](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-github-actions#create-workflow))
    - Uses a service principal to authenticate to Azure
    - Uses the "Azure CLI" action to call your ARM template in your repo

When your workflow completes successfully, go to the Azure portal to see the environment. If everything worked, create the test environment:

4. Copy your `dev` workflow file and use it to create a new workflow file for `test` (`deployTest.yml`)
    - Be sure to update the `paths` in your workflow file (i.e., `.github/workflows/deployTest.yml`)
5. Update the webAppName template parameter (line #6) to `<prefix>devops-test`.

When your workflow completes successfully, go to the Azure portal to see the `test` environment. If everything worked, create the `prod` environment:

6. Copy your `test` workflow file and use it to create a new workflow file for `prod` (`deployProd.yml`)
    - Be sure to update the `paths` in your workflow file (i.e., `.github/workflows/deployProd.yml`)
7. Update the webAppName template parameter (line #6) to `<prefix>devops-prod`.

You should see all three environments in Azure.

### Success Criteria

- Your workflows completes without any errors and you should see all three environments in Azure. 

### Learning Resources

- [What is Infrastructure as Code?](https://docs.microsoft.com/en-us/azure/devops/learn/what-is-infrastructure-as-code)
- [Introduction to GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions/learn-github-actions/introduction-to-github-actions)
- [Understanding workflow path filters](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions#onpushpull_requestpaths)
- [Migrating from Azure Pipelines to GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions#onpushpull_requestpaths)

### Advanced Challenges (optional)

1. In this challenge, we edited the ARM template for each environment (`dev`, `test`, `prod`) but there are ways of [overriding template parameters](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-cli#parameters) when you pass the ARM template to the Azure CLI.

    - Create a fourth environment, called `staging`, by overriding the template parameters in the Azure CLI action. ([hint](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-cli#parameters))
    - When you have successfully created the staging environment, you can delete it as it will not be used in the upcoming challenges. 

2. In this challenge, we setup three separate workflow files to handle `dev`, `test` and `prod`, however, this could be done with a single workflow in conjunction with overriding template parameters and using GitHub secrets. 
    - Create a GitHub secret (called `targetEnv`) and set the *value* to `staging2`
    - In your workflow, read the GitHub secret ([hint](https://docs.github.com/en/free-pro-team@latest/actions/reference/encrypted-secrets))
and pass the value as a overriding template parameter (as described in Advanced Challenge #1)

NOTE: If you are interested in learning more about Infrastructure as Code, there are [multiple](https://github.com/microsoft/WhatTheHack) What the Hacks that cover it in greater depth.

[< Previous](challenge02.md) - [Home](../readme.md) - [Next >](challenge04.md)