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
 - [Challenge 1](./Student/challenge01.md) - GitHub Projects: Track your work
 - [Challenge 2](./Student/challenge02.md) - GitHub Repos: Introduction
 - [Challenge 3](./Student/challenge03.md) - Azure Pipelines: Infrastructure as Code
 - [Challenge 4](./Student/challenge04.md) - Azure Pipelines: Continuous Integration
 - [Challenge 5](./Student/challenge05.md) - Azure Pipelines: Continuous Delivery
 - [Challenge 6](./Student/challenge06.md) - Azure Repos: Branching & Policies
 - [Challenge 7](./Student/challenge07.md) - Azure Monitoring: Application Insights 
 - [Challenge 8](./Student/challenge08.md) - Azure Pipelines: OSS Scanning with WhiteSource Bolt
 - [Challenge 9](./Student/challenge09.md) - GitHub Packages

## Ideas
Kevin does odds. Will does even.

### Challenge 1 - Setup
- Install GitHub desktop

### Challenge 2 - Introductions
- Step 1 create the project, step 2 add issues
- Optional challenge: DevOps Boards + GitHub

### Challenge 3 - GitHub Repos
- Add code to repo
- Clone to local machine
- Make a change and push to GitHub

### Challenge 4 - IaC
- Create the Azure app service via GH action or manually in the portal
- Mention and link to the upcoming ability to manually kick off a workflow

### Challenge 5 - CI
- Create a workflow to build and test and package

### Challenge 6 - CD
- Add steps to deploy to the Azure app service
- Maybe have them do this inside of VS Code 

### Challenge 7 - Branching & policies
- Talk about Branch protection rules https://docs.github.com/en/github/administering-a-repository/about-protected-branches
- Implement feature branches to push a change 
- Use pull request to merge to main
- Choice: use feature branch + master or dev branch (to support phased deployment)

### Challenge 8 - App insights
- Crate and add app insights to project (copy shawn's steps)

### Challenge 9 - Security
- Enable security advisories, dependabot alerts
- Look at code scanning actions in the marketplace (SonarCloud Scan)
- Reference anything GH has on the roadmap

### Challenge 10 - implement GH packages
- Needs to be simple and straightfoward

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