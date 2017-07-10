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

## Commits

### When do I need to commit ?

Commits on the public repository **MUST** follow the atomic approach :
- Commit each fix or task as a separate change
- Only commit when a block of work is complete
- Commit each layout change separately
- Joint commit for layout file, code behind file, and additional resources


The goal is to be able to easily roll back a specific change, without affecting the others. However you **SHOULD NOT** commit unstable work. If you need to commit some unstable code to safeguard your work, do it on a local branch, and clean it up before merging to your master branch and pushing to the remote repository. [This article](https://sandofsky.com/blog/git-workflow.html) provides some good guidelines on the subject.

### How do I write my commits

Here are 7 rules you **MUST** respect when writing a commit :
- Separate subject from body with a blank line
- Limit the subject line to 50 characters
- Capitalize the subject line
- Do not end the subject line with a period
- Use the imperative mood in the subject line
- Wrap the body at 72 characters
- Use the body to explain what and why vs.

A good rule of thumb is to check if your commit subject could complete the sentence "If applied, this commit will..."

Ex :
- `If applied, this commit will changing behavior of X` :x:
- `If applied, this commit will more fixes for broken stuff` :x:
- `If applied, this commit will remove deprecated methods` :white_check_mark:

You can find more on the subjects [in this article](https://chris.beams.io/posts/git-commit/) from which this guidelines are taken.
