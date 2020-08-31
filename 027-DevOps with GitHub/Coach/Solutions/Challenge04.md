# (Solutions) What The Hack - DevOps with GitHub

# Challenge 4 - Continuous Integration

[< Previous Challenge](./Challenge03.md) - **[Home](../readme.md)** - [Next Challenge>](./Challenge05.md)



## Students should:

1. From the GitHub respository, click the 'Actions' tab. In this tab, students will see a variety of pre-defined starter workflows, or the option to create one from scratch. 

1. Select the starter workflow labeled '.NET Core'. This will provide students with the default workflow for .NET Core which should include steps to restore, build, and test the application. It should also include a 'master' branch trigger by default.

1. Click the green 'Start commit button,' enter a commit message, and select 'Commit new file'.

1. Follow similar steps to challenge 2 in making a small change to the repository, and push this change to GitHub. From the 'Actions' tab, students should see a new workflow run which was triggered by this change. Watch the run to ensure CI completes as expected. 

EXAMPLE WORKFLOW FILE:

    name: .NET Core

    on:
        push:
            branches: [ master ]
        pull_request:
            branches: [ master ]

    jobs:
        build:

            runs-on: ubuntu-latest

            steps:
            - uses: actions/checkout@v2
            - name: Setup .NET Core
              uses: actions/setup-dotnet@v1
              with:
                dotnet-version: 3.1.301
            - name: Install dependencies
              run: dotnet restore
            - name: Build
              run: dotnet build --configuration Release --no-restore


## Advanced Challenge

1. The `dotnet test` command is included in the workflow yaml by default if students began with the starter template. If they removed this step or wrote the workflow from scratch, ensure they add something similar to the follow at the end of the file:

        - name: Test
          run: dotnet test --no-restore --verbosity normal