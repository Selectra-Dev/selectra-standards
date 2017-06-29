# How we use GitHub for our projects

## work-flows

- Default work-flows
- Extended work-flows

We use two different work-flows depending on the project size. For most of our projects with stick to the one we refer to as "Default work-flows". However, for bigger project, it might be better to use the extended one.

The choice of either of this work-flows is open to discussion, but **MUST** be made in agreement with the whole developing team and the sysadmin.

The chosen work-flow **MUST** be one of this two choices. Having consistent use on how to use GitHub across our projects helps preventing mistakes, and make the developers work easy.

### Default work-flows

By default, we simply follow GitHub guidelines :
- The shared repository on GitHub has one permanent branch : master. What's on this branch **MUST** always be deployable ;
- When working on a new fix or feature the developer **MUST** create a new branch on the shared repository. It is **RECOMMENDED** that the developer commits his work on this branch regularly so we can keep a history of what's been done ;
- When the code is ready to be deployed, or the developer wants to discuss some stuff concerning the new features, he **MUST** create a pull requests. He **MUST NOT** merge directly to master ;
- When the team agrees on the changes, the sysadmin merge the branch to master.

The guidelines can be found [here](https://guides.GitHub.com/introduction/flow/).

### Extended work-flow

For some project, it might be useful to use a more complex work-flow. The complete guideline is available [here](http://nvie.com/posts/a-successful-git-branching-model/)

## Some standards

  ### commits

  The commits **MUST** all be written using the following template :
