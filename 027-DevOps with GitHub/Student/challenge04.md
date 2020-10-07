# What The Hack - DevOps with GitHub

# Challenge 4 - Continuous Integration

[< Previous](challenge03.md) - [Home](../readme.md) - [Next >](challenge05.md)


## Introduction

With our existing repository and newly-created Azure App Service, we have laid the foundation for our application. Now, we must connect our source code and its destination. The first step in this journey is called Continuous Integration. 

Continous Integration is the process of merging local code changes into source control and may include steps to automatically build and/or test the code. When done effectively, Continuous Integration allows developers to rapidly iterate and collaborate, and it helps ensure that newly added code does not break the current application. 


## Description

In this section, you will use GitHub Actions to define a build pipeline for Continuous Integration.

Begin by creating a new workflow YAML file and adding it to your repository. This pipeline should be triggered by code changes to the main/master branch of your repository. It should also include steps to build the application.

Once you have created the pipeline, make a small change to the application code (add a comment, newline, etc). Commit and push this change, then watch the Action complete to ensure the workflow runs as expected.


## Success Criteria

You should see a successful workflow run. Ensure that the workflow trigger reads 'on:push' into the 'main' or 'master' branch. 

View the workflow logs to see successful completion of each step, including building the application.


## Learning Resources

- For general information about continuous integration, check [here](https://docs.github.com/en/actions/building-and-testing-code-with-continuous-integration/about-continuous-integration). To see more specific instructions for setting up workflows, check [here](https://docs.github.com/en/actions/building-and-testing-code-with-continuous-integration/setting-up-continuous-integration-using-github-actions). 
- For more information about workflows and triggers, check [here](https://docs.github.com/en/actions/configuring-and-managing-workflows/configuring-a-workflow). 
- Check out [this GitHub repository](https://github.com/actions/setup-dotnet) for more information about using dotnet commands in a workflow.


## Tips

- If you are having trouble finding a starting point, try clicking over to the 'Actions' tab of your GitHub repository. 
- Additionally, try to take advantage of the prebuilt workflow templates if you find one that might work! 


## Advanced Challenges

As part of the application, we provided a series of unit tests. Try adding step(s) to your workflow in order to run these tests on your code! (As a hint, you would want to use [this command](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-test) to run unit tests on a .NET Core application.)

Adding automated tests to the CI process can help prevent errors from ever reaching production. Thus, writing and running unit tests is considered a DevOps best practice.

[< Previous](challenge03.md) - [Home](../readme.md) - [Next >](challenge05.md)