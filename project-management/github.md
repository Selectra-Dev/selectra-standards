# How we use GitHub for our projects

## Our workflows

- Default workflows
- Extended workflows

We use two different types of workflow depending on the project size. For most of our projects, we stick to the one we refer to as "Default workflows". However, for bigger projects, we might opt for the extended one.

The choice of either of these workflows is open to discussion, but **MUST** be made in agreement with the whole developing team and the sysadmin.

The chosen workflow **MUST** be one of these two choices. Having consistent use of GitHub across our projects helps preventing mistakes, and makes the developer's work easier.

### Default workflows

By default, we simply follow GitHub guidelines:
- The shared repository on GitHub has one permanent branch: master. The content of this branch **MUST** always be deployable;
- When working on a new fix or feature, the developer **MUST** create a new branch on the shared repository. It is **RECOMMENDED** that the developer commits his work on this branch regularly in order to keep a clean and useful history;
- When the code is ready to be deployed, or when the developer wants to discuss some details concerning new features, he **MUST** create a pull request. He **MUST NOT** merge directly to master;
- When the team agrees on the changes, the project manager merges the branch into master.

The guidelines can be found [here](https://guides.GitHub.com/introduction/flow/).

### Extended workflow

For some projects, it might be useful to use a more complex workflow. The complete guideline is available [here](http://nvie.com/posts/a-successful-git-branching-model/)

## Some standards

  ### commits

  The commits **MUST** all be written using the following template:
