# How we use github for our projects

## Workflows

- Default workflows
- Extended workflows

We use two different workflows depending on the project size. For most of our projects with stick to the one we refer to as "Default workflows". However, for bigger project, it might be better to use the extended one.

The choice of either of this workflows is open to discussion, but **MUST** be made in agreement with the whole developping team and the sysadmin.

The chosen wokflow **MUST** be one of this two choices. Having consistent use on how to use github across our projects helps preventing mistakes, and make the developpers work easy.

### Default workflows

By default, we simply follow github guidelines :
- The shared repository on github has one permanent branch : master. What's on this branch **MUST** always be deployable
- When working on a new fix or feature the developer creates a new branch on the shared repository. It is **RECOMMENDED** that the developer commits his work on this branch regularly so we can keep a history of what's been done.
- When the code is ready to be deployed, or the developer wants to discuss some stuff concerning the new features, he **MUST** creates a pull requests. He **MUST NOT** merge directly to master
- When the team agrees on the changes, the sysadmin merge the branch to master

### Extended workflow

For some project, it might be useful to use a more complex workflow. The complete guideline is available [here](http://nvie.com/posts/a-successful-git-branching-model/)

## Some standards

  ### commits

  The commits **MUST** all be written using the following template :
