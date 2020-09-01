# (Solutions) What The Hack - DevOps with GitHub

# Challenge 6 - Branching and Policies

[< Previous Challenge](./Challenge05.md) - **[Home](../readme.md)** - [Next Challenge>](./Challenge07.md)


## Students should:

1. Enter the 'Settings' tab and click 'Branches.' Here they can create a branch protection rule by selecting 'Add Rule' and entering a branch name and desired policies. 

1. Create a feature branch. This can be done in a couple of ways, either through the GUI Git client, or by using the following set of local commands:

        git checkout -b {branchName}
        
        git push origin {branchName}

1. Make a code change similar to challenge 4, and push the change to the GitHub repository using git add, commit, and push commands.

1. Create a Pull Request by visiting the 'Pull requests' tab in GitHub. Click on the 'New pull request' button, select the relevant branch to compare, and click the 'Create pull request button'. 

1. Wait for the PR checks to complete, and merge the branches. After merging, feel free to select the button which deletes the feature branch. 


## Advanced Challenge

1. Using the steps mentioned above, students should create a branch off of `master` or `main` called `development`. From here, the steps are very similar to the above. The main difference is that we will want to create a feature branch off of `development` rather than `master` or `main`. In this case, we use a command similar to the following:

        git checkout -b {featureBranchName} development

IMPORTANT: Do not delete the development branch after completing the deployment. You will want to use this same branch to repeat the process for your next deployment. 