# What The Hack - DevOps with GitHub

# Challenge 4 - Continuous Integration

[< Previous Challenge](./Challenge03.md) - **[Home](../readme.md)** - [Next Challenge>](./Challenge05.md)

## Pre-requisites (Optional)

*Include any technical pre-requisites needed for this challenge.  Typically, it is completion of one or more of the previous challenges if there is a dependency.*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit.**

**- Fusce commodo nulla elit, vitae scelerisque lorem maximus eu.** 

**- Nulla vitae ante turpis. Etiam tincidunt venenatis mauris, ac volutpat augue rutrum sed. Vivamus dignissim est sed dolor luctus aliquet. Vestibulum cursus turpis nec finibus commodo.**

**- Vivamus venenatis accumsan neque non lacinia. Sed maximus sodales varius. Proin eu nulla nunc. Proin scelerisque ipsum in massa tincidunt venenatis. Nulla eget interdum nunc, in vehicula risus.**


## Introduction (Optional)

With our existing repository and newly-created Azure App Service, we have laid the foundation for our application. Now, we must connect our source code and its destination. The first step in this process is called Continuous Integration. 

Continous Integration is the process of merging local code changes into source control and may include steps to automatically build and/or test the code. When done effectively, Continuous Integration allows developers to rapidly iterate and collaborate, and it helps ensure that newly added code does not break the current application. 


## Description

In this section, you will use GitHub Actions to define a build pipeline for Continuous Integration.

Begin by creating a new workflow YAML file and adding it to your repository. This pipeline should be triggered by code changes to the main/master branch of your repository. It should also include steps to build the application.

Once you have created the pipeline, make a small change to the application code (add a comment, newline, etc). Commit and push this change, then watch the Action complete to ensure the workflow runs as expected.

*The challenge description and details go here.  This should NOT be step-by-step but rather a simple stating of the technical goals of the challenge.  If this is more than 2-3 paragraphs, it's likely you are not doing it right.*

*Optionally, you may provide learning resources and/or tips and code snippets in the sections below. These are meant  as learning aids for the attendees to help them complete the challenge and maintain momentum as they may fall behind the rest of their squad cohorts.*


## Success Criteria

You should see successful workflow run. Ensure that the workflow trigger reads 'on:push' into the 'main' or 'master' branch. View the workflow logs to see successful completion of each step.

*Success criteria goes here. This is a list of things an coach can verfiy to prove the attendee has successfully completed the challenge.*




## Learning Resources

*List of relevant links and online articles that should give the attendees the knowledge needed to complete the challenge.*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit.**

**- Fusce commodo nulla elit, vitae scelerisque lorem maximus eu.** 

**- Nulla vitae ante turpis. Etiam tincidunt venenatis mauris, ac volutpat augue rutrum sed. Vivamus dignissim est sed dolor luctus aliquet. Vestibulum cursus turpis nec finibus commodo.**


## Tips (Optional)

*Add tips and hints here to give students food for thought.*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit.**

**- Fusce commodo nulla elit, vitae scelerisque lorem maximus eu.** 


## Advanced Challenges (Optional)

TESTING

*Too comfortable?  Eager to do more?  Try these additional challenges!*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo nulla elit, vitae scelerisque lorem maximus eu. Nulla vitae ante turpis. Etiam tincidunt venenatis mauris, ac volutpat augue rutrum sed. Vivamus dignissim est sed dolor luctus aliquet. Vestibulum cursus turpis nec finibus commodo. Vivamus venenatis accumsan neque non lacinia.**

**- Sed maximus sodales varius. Proin eu nulla nunc. Proin scelerisque ipsum in massa tincidunt venenatis. Nulla eget interdum nunc, in vehicula risus. Etiam rutrum purus non eleifend lacinia. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quis vestibulum risus. Maecenas eu eros sit amet ligula consectetur pellentesque vel quis nisi.**