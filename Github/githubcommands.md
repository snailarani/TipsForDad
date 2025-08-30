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

## Git Commands
