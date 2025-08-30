# About Git/GitHub

## Intro

**Git** is a version control software that lets you track changes to your code over time. **GitHub** is a web platform that allows users to use Git **collaboratively**, and stores your Git code remotely.

## Repositories

A **repository** (or repo) is a space/folder where a particular project is stored. Repositories are tracked by Git.

There are 2 types of repositories:

1. **Local Repository** - This kind of repository is stored on your local device. You can add changes to you local repository and **push** them to a remote repository.
2. **Remote Repository** - These repositories can be found on [https://github.com/](https://example.com). You can clone these repositories onto your own device.

### Creating a Repo

You can create a repo from your local device, or from Github.

#### Creating a Repo from a local project

First, select the folder you would like Git to track, then navigate to that folder (using the `cd` command). This folder can already have existing files/code in it.

<!-- Video example -->

Then, in the terminal, use the command: `git init`

This will make Git track your folder. Now you can make changes, make commits, and it will all be tracked by Git.

#### Creating a Repo from GitHub

Log into your github account. Select the '+' sign on the banner at the top of the page. Then select 'new repository'. From there you can give your repo a name, and set some configurations.

To clone this repository onto your local device (so you can start adding code), select the drop down next to the blue button which says 'code'. This will give you a link to the repo.

In your terminal, navigate to where you would like to store this repo. Then use the command: `git clone [link_to_repo]`.

Now you can start adding code to this repo from your own device.

<!-- Video example -->


## Branches

<!-- TODO -->

## Git Commands

When making changes to a local repo, you can choose what changes you would like git to track, as well as being able to go back to older versions of your repo.

### git add

When you have made changes that you would like git to track, use the command `git add [file_name]`. This will 'stage' the specified file(s) in your repo. Essentially, this tells git which files to commit/store.

Typically, you would use the command `git add .`. The `.` means all files in the repository - including new files you have made since the last commit.

### git commit

Once you have 'staged' the files you want to store, (once you have run `git add`), use the command `git commit` to make git permanently store these changes as part of the repository's history. Usually, git will force you to add a 'commit message' when you make a commit. The usual format for this command is: `git commit -m[message_describing_the_new_changes]`.

### git merge

<!-- TODO -->

### git push

If your branch has an 'upstream' (i.e if your branch is tracking a branch on a remote repo), you can use the command `git push` to 'push' your new changes to the remote repository. Git will only push **committed changes**, so make sure you commit all the changes you want to see on the remote branch (git will usually remind you if you have uncommitted changes).

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
