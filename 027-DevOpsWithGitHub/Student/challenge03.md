# What the Hack: DevOps with GitHub 

## Challenge 3 - Infrastructure as Code
[< Previous](challenge02.md) - [Home](../readme.md) - [Next >](challenge04.md)

### Introduction

Great we now have some code, now we need an environment to deploy it to. The term "Infrastructure as Code" refers to using templates (code) to repeatedly and consistently create the dev, test, prod (infrastructure) environments. We can automate the process of deploying the Azure services we need with an Azure Resource Manager (ARM) template. 

Review the following articles:

- [Azure Resource Manager overview](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview)
- [Create Azure Resource Manager template](https://docs.microsoft.com/en-us/azure/azure-resource-manager/how-to-create-template)


### Challenge

We can use GitHub Actions to automate the deployment of our Azure infrastructure. For our application, we will deploy 3 environments: Dev, Test and Prod. Each environment will have its own Web App, however all of our environments will share a single Resource Group, App Service Plan, Application Insights instance, and Azure Container Registry. NOTE: in real deployments, you will likely not share all of these resources.

First, we are going to deploy the dev environment:

1. Review the [ARM template](./Code/ARM-Templates/container-webapp-template.json). It defines a number of parameters and uses them to create the Resource Group, App Service Plan, Web App, Application Insights, and Azure Container Registry.
2. Update the [ARM template](./Code/ARM-Templates/container-webapp-template.json), replacing the `<prefix>` part with a unique lowercase 5 letter name.
3. Create a GitHub workflow (named deployDev.yml) that accomplishes the following ([hint](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-github-actions)):
    - Only runs when changes are made to the workflow file itself or the [ARM template](./Code/ARM-Templates/container-webapp-template.json) in your repo ([hint](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-github-actions#create-workflow))
    - Uses a service principal to authenticate to Azure
    - Uses the "Azure CLI" action to call your [ARM template](./Code/ARM-Templates/container-webapp-template.json) in your repo

When your workflow completes successfully, go to the Azure portal to see the environment. If everything worked, create the test environment:

1. Copy your dev workflow file and use it to create a new workflow file for `test`
    - Be sure to update the `paths` in your workflow file (i.e., ".github/workflows/deployTest.yml")
2. Update the webAppName template parameter (line 6 in the [ARM template](./Code/ARM-Templates/container-webapp-template.json)) to `<prefix>devops-test`.

When your workflow completes successfully, go to the Azure portal to see the test environment. If everything worked, create the prod environment:

1. Copy your test workflow file and use it to create a new workflow file for `prod`
    - Be sure to update the `paths` in your workflow file (i.e., ".github/workflows/deployProd.yml")
2. Update the webAppName template parameter (line 6 in the [ARM template](./Code/ARM-Templates/container-webapp-template.json)) to `<prefix>devops-prod`.

You should see all three environments in Azure.

### Success Criteria

1. Your infrastructure release should complete without any errors and you should see all three environments out in Azure. 

> NOTE: We are just scratching the surface of what is offered in Azure for Infrastructure as Code, if you are interested in learning more there is a full What the Hack focused on Azure Infrastructure as Code.

[< Previous](challenge02.md) - [Home](../readme.md) - [Next >](challenge04.md)