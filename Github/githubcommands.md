# About Git/GitHub

## Intro

**Git** is a version control software that lets you track changes to your code over time. **GitHub** is a web platform that allows users to use Git **collaboratively**, and stores your Git code remotely.

## Repositories

A **repository** (or repo) is a space/folder where a particular project is stored. Repositories are tracked by Git.

There are 2 types of repositories:

1. **Local Repository** - This kind of repository is stored on your local device. You can add changes to you local repository and **push** them to a remote repository.
2. **Remote Repository** - These repositories can be found on [https://github.com/](https://example.com). You can clone these repositories onto your own device.

### Creating a Repo

You can create a repository from your local device, or from Github.

#### Creating a Repo from a local project

First, select the folder you would like Git to track, then navigate to that folder (using the `cd` command). This folder can already have existing files/code in it.

<!-- Video example -->

Then, in the terminal, use the command: `git init`

This will make Git track your folder. Now you can make changes, make commits, and it will all be tracked by Git.

#### Creating a Repo from GitHub

Log into your github account. Select the '+' sign on the banner at the top of the page. Then select 'new repository'. From there you can give your repository a name, and set some configurations.

To clone this repository onto your local device (so you can start adding code), select the drop down next to the blue button which says 'code'. This will give you a link to the repository.

In your terminal, navigate to where you would like to store this repository. Then use the command: `git clone [link_to_repo]`.

Now you can start adding code to this repository from your own device.

<!-- Video example -->


## Branches

Typically, if you are working on a large project, or a team project, each feature will be developed on a different `branch`. Branches will then be merged together once that particular feature is complete.

### Remote and Local branches

Like repositories, there are 2 kinds of branches - remote and local. Local branches live on your local device in your local repository, and remote branches live on the remote repository on github. Both branches should have the same name. You can then link these branches to update changes between them.

Typically, you will have a local branch and a remote branch for 1 feature. The local branch (on your device), is where you add the code. The remote branch (on github) is where that worked can be shared with other developers. You cannot edit code on the remote branch directly. It must be done on the local branch, then you update the remote branch.

### Remote tracking

To link a remote and local branch, 

### git branch

To create a local branch in your local repository, use the command `git branch [branch_name]`. To see all current local branches, use the command `git branch`. This will also tell you what branch you are currently working on.

### git checkout

To switch between different local branches, use the command `git checkout [branch_name]`.

### Main Branch

In git, the `main` or `master` branch is the default branch that git will create for you to work on when you create your repository. In large development projects, the `main` branch usually contains the code that is ready for production.

Usually, a new branch will be made for a feature. Once that feature is complete, the branch is merged into the `main` branch. Multiple features are developed in parallel, and are all merged into `main`. This is how production code is slowly built up.

Because the `main` branch contains the code that is ready for production, **you must not develop code on the main branch**, as there is a risk of your code accidentally being overwritten by someone else when they try to merge their branch into main. Always create a new branch, develop code on here, then merge these changes into main.

### Pull Requests

Most projects will have protection on their **remote `main` branch**. This prevents you from merging your code into the `main` branch directly. To merge your code onto the remote `main` branch, you will have to open a `pull request`. This can be done through github.com. When you open a pull request, other developers will be able to review your code before merging your changes into the production code.

## Git Commands

When making changes to a local repository, you can choose what changes you would like git to track, as well as being able to go back to older versions of your repository.

### git add

When you have made changes that you would like git to track, use the command `git add [file_name]`. This will 'stage' the specified file(s) in your repository. Essentially, this tells git which files to commit/store.

Typically, you would use the command `git add .`. The `.` means all files in the repository - including new files you have made since the last commit.

### git commit

Once you have 'staged' the files you want to store, (once you have run `git add`), use the command `git commit` to make git permanently store these changes as part of the repository's history. Usually, git will force you to add a 'commit message' when you make a commit. The usual format for this command is: `git commit -m[message_describing_the_new_changes]`.

### git merge

If you would like to combine code from 2 different branches on your local device, you can use the `git merge` command. Git will determine how it combines the code from both branches. If there is a risk of overwriting code from either branch during a merge, git will produce an error called a `merge conflict`. You must manually resolve merge conflicts before you can merge 2 branches. (This can be done in vscode directly)

### git push

If your branch has an 'upstream' (i.e if your branch is tracking a branch on a remote repository), you can use the command `git push` to 'push' your new changes to the remote repository. Git will only push **committed changes**, so make sure you commit all the changes you want to see on the remote branch (git will usually remind you if you have uncommitted changes).

By default git will push changes to the remote branch which your branch is tracking. But you can specify other branches to push your changes to.

### git pull

Likewise, if your branch has an upstream, you can run `git pull` to 'pull' any updates from the remote branch onto your local branch. Like before, git will want you to commit any new changes on your local branch before you pull, to make sure none of your changes are overwritten.

By default git will pull changes from the remote branch which your branch is tracking. But you can specify other branches to pull your changes from.

When you are working on a team project with a remote repository, the usual flow of commands goes like this:

1. `git checkout main`
2. `git pull`
3. `git checkout [your_branch]`
4. `git merge main`
5. [make your changes]
6. `git add .`
7. `git commit -m [..]`
8. `git push`

### Table of Commands

| Number | Command |  Description |
| ------ | ------- | --------- |
| 1 | `git add [file_name]` | |
| 2 | `git commit` | |
| 3 | `git push origin [source]:[destination]` | |
| 4 | `git pull origin [source]:[destination]` | |
| 5 | `git merge [branch_name]` | |
| 6 | `git checkout [branch_name]` | |
| 7 | `git branch` | List all branches |
| 8 | `git log` | |
