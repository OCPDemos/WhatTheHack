# What The Hack - DevOps with GitHub

# Challenge 6 - Branching and Policies

[< Previous Challenge](./Challenge05.md) - **[Home](../readme.md)** - [Next Challenge>](./Challenge07.md)

## Pre-requisites (Optional)

*Include any technical pre-requisites needed for this challenge.  Typically, it is completion of one or more of the previous challenges if there is a dependency.*


## Introduction (Optional)

*Provide an overview of the technologies or tasks that will be needed to complete the next challenge.  This includes the technical context for the challenge, as well as any new "lessons" the attendees should learn before completing the challenge.*

*Optionally, the coach or event host may present a mini-lesson (with a PPT or video) to set up the context & introduction to the next topic.*

In the previous steps, we successfully implemented an end-to-end CI/CD pipeline! However, our current workflow will immediately promote every small change directly to production. Typically, you would want to avoid working directly against the main branch in your repository to avoid conflicts or protect the production environment. Enter, branching!




## Description

In this challenge, you will create a branch protection rule which prevents changes from being commited directly to your main branch. Then, you will use a feature branch to update the code and merge your change into the protected branch. 

First, create a branch protection rule which prevents developers from commiting changes to the main branch in the repository.

Next, create a feature branch, make a small change to the code, and sync this branch with the GitHub repository.

Finally, create and complete a Pull Request, merging your code change into the protected branch. 

*The challenge description and details go here.  This should NOT be step-by-step but rather a simple stating of the technical goals of the challenge.  If this is more than 2-3 paragraphs, it's likely you are not doing it right.*

*Optionally, you may provide learning resources and/or tips and code snippets in the sections below. These are meant  as learning aids for the attendees to help them complete the challenge and maintain momentum as they may fall behind the rest of their squad cohorts.*


## Success Criteria

In GitHub, you should be able to view the branch protection rule which prevents chances from being commited to your main branch. 

Additionally, check the Pull Requests tab to view the 'closed' Pull Request which merged changes from the feature branch into the main branch.

*Success criteria goes here. This is a list of things an coach can verfiy to prove the attendee has successfully completed the challenge.*


## Learning Resources

*List of relevant links and online articles that should give the attendees the knowledge needed to complete the challenge.*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit.**

**- Fusce commodo nulla elit, vitae scelerisque lorem maximus eu.** 

**- Nulla vitae ante turpis. Etiam tincidunt venenatis mauris, ac volutpat augue rutrum sed. Vivamus dignissim est sed dolor luctus aliquet. Vestibulum cursus turpis nec finibus commodo.**


## Tips (Optional)

REPO NEEDS TO BE PUBLIC IF ON GITHUB FREE

*Add tips and hints here to give students food for thought.*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit.**

**- Fusce commodo nulla elit, vitae scelerisque lorem maximus eu.** 


## Advanced Challenges (Optional)

Use master + dev branch in order to do more advanced, phased deployments

*Too comfortable?  Eager to do more?  Try these additional challenges!*

**- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo nulla elit, vitae scelerisque lorem maximus eu. Nulla vitae ante turpis. Etiam tincidunt venenatis mauris, ac volutpat augue rutrum sed. Vivamus dignissim est sed dolor luctus aliquet. Vestibulum cursus turpis nec finibus commodo. Vivamus venenatis accumsan neque non lacinia.**

**- Sed maximus sodales varius. Proin eu nulla nunc. Proin scelerisque ipsum in massa tincidunt venenatis. Nulla eget interdum nunc, in vehicula risus. Etiam rutrum purus non eleifend lacinia. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed quis vestibulum risus. Maecenas eu eros sit amet ligula consectetur pellentesque vel quis nisi.**