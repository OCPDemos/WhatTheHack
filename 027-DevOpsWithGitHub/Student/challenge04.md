# What The Hack - DevOps with GitHub

## Challenge 4 - Continuous Integration (CI)

[< Previous](challenge03.md) - [Home](../readme.md) - [Next >](challenge05.md)

### Introduction

With our existing repository and newly-created Azure App Service, we have laid the foundation for our application. Now, we must connect our source code and its destination. The first step in this journey is called Continuous Integration (CI). 

Continous Integration is the process of merging local code changes into source control and may include steps to automatically build and/or test the code. When done effectively, Continuous Integration allows developers to rapidly iterate and collaborate, and it helps ensure that newly added code does not break the current application. 

Review the following articles:
- [About continuous integration](https://docs.github.com/en/actions/building-and-testing-code-with-continuous-integration/about-continuous-integration)
- [Setting up continuous integration using workflow templates](https://docs.github.com/en/actions/building-and-testing-code-with-continuous-integration/setting-up-continuous-integration-using-github-actions)

### Challenge

In this challenge, you will build and test the .NET Core application, build a container image and push it to Azure Container Registry (ACR). 

1. Create a new `.NET Core` workflow from the GitHub Actions marketplace ([hint](https://github.com/actions/starter-workflows/blob/dacfd0a22a5a696b74a41f0b49c98ff41ef88427/ci/dotnet-core.yml))
2. Configure path filters to *only* trigger this workflow for changes in the `/Application` folder
    
3. Review and update the predefined steps used to build the .NET Core application (note: for each step below, you may need to update each command to pass the path to the  `.csproj` as an argument):
   - `restore` - will get all the dependencies. Update with an [argument](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-build#arguments) to the application csproj file: `./Application/aspnet-core-dotnet-core/aspnet-core-dotnet-core.csproj`
   - `build` - will actually compile our code. Update with an [argument](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-build#arguments) to the application csproj file: `./Application/aspnet-core-dotnet-core/aspnet-core-dotnet-core.csproj`
   - `test` - will execute all our unit tests. Update with an [argument](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-build#arguments) to the unit test csproj file: `./Application/aspnet-core-dotnet-core.UnitTests/aspnet-core-dotnet-core.UnitTests.csproj` 

4. Test the workflow by making a small change to the application code (i.e., add a comment). Commit, push and ensure the workflow completes successfully.

At this point, any changes pushed to the `/Application` folder automatically triggers the workflow...and that is Continuous Integration! Now, we need to extend our workflow with steps to build a container image and push it to the registry.

5. Add a GitHub Action to your workflow to build and push the container image to the registry ([hint](https://github.com/marketplace/actions/build-and-push-docker-images))
    - To authenticate to ACR, you may need to get the username and password to your ACR instance and save as GitHub secrets ([hint](https://docs.microsoft.com/en-us/azure/container-registry/container-registry-authentication#admin-account))
    - Key parameters to configure for Docker:
        - `dockerfile` - The path to the Dockerfile - a critical parameter. You will need to point to the Dockerfile in the `/Application` folder.
        - `username` - Used to login to ACR. You will need to read from the GitHub secret you created.
        - `password` - Used to login to a ACR. You will need to read from the GitHub secret you created.
        - `registry` - Server address of Docker registry. Set this to "`registryName`.azurecr.io" - replacing `registryName` with the `<prefix>devopsreg` value in your ARM template file (line #26).
        - `repository` - The repository (or 'folder') to target in the registry. Set this to "`imageName`.azurecr.io" - replacing `imageName` with the `<prefix>devopsimage` value in your ARM template file (line #31).
        - `tags` - This needs to be a unique value each time, as this is used to version the images in the repository. GitHub makes [environment variables](https://docs.github.com/en/free-pro-team@latest/actions/reference/context-and-expression-syntax-for-github-actions#github-context) available that helps with this. Set `tags` to `${{ GITHUB_RUN_NUMBER }}`.

6. Test the workflow by making a small change to the application code (i.e., add a comment). Commit, push, monitor the workflow and verify that a new container image is built, uniquely tagged and pushed to ACR after each successful workflow run.

### Success Criteria

- Any changes pushed to the `/Application` folder automatically triggers the workflow 
- .NET Core restore, build and test steps completes successfully
- A new container image is built, uniquely tagged and pushed to ACR after each successful workflow run

### Learning Resources

- [Introduction to GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions/learn-github-actions/introduction-to-github-actions)
- [Understanding workflow path filters](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions#onpushpull_requestpaths)
- [dotnet commands](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet#dotnet-commands)

### Tips

- If you are having trouble finding a starting point, try clicking over to the 'Actions' tab of your GitHub repository. 
- Take advantage of the prebuilt workflow templates if you find one that might work! 

### Advanced Challenges (optional)

1. In this challenge, if the workflow fails, an email is set to the repo owner. Sometimes, you may want to log or create a GitHub issue when the workflow fails.
    - Add a step to your workflow to create a GitHub issue when there is a failure.

[< Previous](challenge03.md) - [Home](../readme.md) - [Next >](challenge05.md)