# What The Hack - DevOps with GitHub

## Introduction
DevOps is a journey not a destination. Our goal when writing this challenged based hack is to introduce you to GitHub and some common DevOps practices. We also understand that your choice of programming language and DevOps processes might differ from the ones we will be using in this hack, that is OK. Our intent was to select some of the most common programming languages and highlight industry best practices, with an emphasis on showing how GitHub can help you on your DevOps journey, so that you can apply this in your environment with the languages and tools that you use.

## Learning Objectives

This hack will help you learn:

1. How to use GitHub to manage source control
1. How to use GitHub for Project Management
1. How to use GitHub Actions for CI & CD
1. Monitoring apps with Application Insights

## Challenges
 - [Challenge 0](./Student/challenge00.md) - Setup and Introduction
    - Install GitHub desktop  
 - [Challenge 1](./Student/challenge01.md) - Track your work with GitHub Project Boards
    - Create the project
    - Add issues for each challenge
    - Optional challenge: DevOps Boards + GitHub 
 - [Challenge 2](./Student/challenge02.md) - Centralize your code with GitHub Repos
    - Add code to repo
    - Clone to local machine
    - Make a change and push to GitHub
 - [Challenge 3](./Student/challenge03.md) - Azure Pipelines: Infrastructure as Code
    - Create the Azure app service via GH action or manually in the portal
    - Mention and link to the upcoming ability to manually kick off a workflow
 - [Challenge 4](./Student/challenge04.md) - Azure Pipelines: Continuous Integration
    - Add steps to deploy to the Azure app service
    - Maybe have them do this inside of VS Code 
 - [Challenge 5](./Student/challenge05.md) - Azure Pipelines: Continuous Delivery
    - Create a workflow to build and test and package
 - [Challenge 6](./Student/challenge06.md) - Azure Repos: Branching & Policies
    - Talk about Branch protection rules https://docs.github.com/en/github/administering-a-repository/about-protected-branches
    - Implement feature branches to push a change 
    - Use pull request to merge to main
    - Choice: use feature branch + master or dev branch (to support phased deployment) 
 - [Challenge 7](./Student/challenge07.md) - Azure Monitoring: Application Insights
    - Create and add app insights to project (copy shawn's steps)
 - [Challenge 8](./Student/challenge08.md) - Azure Pipelines: OSS Scanning with WhiteSource Bolt
    - Enable security advisories, dependabot alerts
    - Look at code scanning actions in the marketplace (SonarCloud Scan)
    - Reference anything GH has on the roadmap
 - [Challenge 9](./Student/challenge09.md) - GitHub Packages
    - Needs to be simple and straightfoward


## Ideas
Kevin does odds. Will does even.

## Prerequisites
- Your own Azure subscription with Owner access
- [Visual Studio Code](https://code.visualstudio.com)
- [Git SCM](https://git-scm.com/download)

## Repository Contents (Optional)
- `../Student`
  - Student Challenge Guides
- `../Student/Resources`
  - Student's resource files, code, and templates to aid with challenges

## Contributors
- Kevin M. Gates
- Will Fox