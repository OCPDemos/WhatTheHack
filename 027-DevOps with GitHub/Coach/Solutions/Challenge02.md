# (Solutions) What The Hack - DevOps with GitHub

# Challenge 2 - Repositories

[< Previous Challenge](./Challenge01.md) - **[Home](../readme.md)** - [Next Challenge>](./Challenge03.md)


## Students should:

1. On the main page of the new repository (top right), the students should see a green button which says 'Code'. Clicking the button should open a drop-down which includes a link to the repository and a button reading 'Open with GiHub Desktop'. For those using the GUI, click the 'Open with GitHub Desktop'. For those using the command line, use a command like `git clone https://github.com/{yourRepositoryName}`

    Note: If using the command line tool for the first time, students may need some assistance with [configuration](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup). 

1. Download and unzip the application from [here](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/microsoft/WhatTheHack/tree/master/014-OSSDevOps/Student/Resources/Challenge-03/app). Cloning the repository should have created a local directory representing the repo. Copy the application into the root of this directory. 

1. Commit the changes to GitHub. Executing from the root directory of the local repo, students should run the following git commands (or similar):

        git add .

        git commit -m "Commit Message"

        git push origin master

    The GUI should have equivalent commands for adding+commiting changes (including a commit message) and pushing to the central repository.


## Advanced Challenge

1. There are a couple options for the advanced challenge. If students are working as a group on a single GitHub repository, encourage another student to clone the repository, make a code change, and follow the above steps to push that change to GitHub. If instead students are working on their own repos, encourage the students to make changes via the editor on the GitHub website (click on a file, and use the pencil button at the top right of the file). 

1. Once an edit has been made, students should use the `git pull` command to see changes reflected locally. 