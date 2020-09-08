# Contributing

## Steps to follow

### 1. Fork it

You can get your own fork/copy of [community-website](https://github.com/we-developers-community/community-website) by using the <kbd><b>Fork</b></kbd> button.

 [![Fork Button](https://help.github.com/assets/images/help/repository/fork_button.jpg)](https://github.com/we-developers-community/community-website)

### 2. Clone it

You need to clone (download) it to local machine using

```sh
$ git clone https://github.com/<YOUR_USERNAME>/community-website.git
```

> This makes a local copy of repository in your machine.

Once you have cloned the repository, move to that folder first using change directory command.

```sh
# This will change directory to a folder community-website
$ cd community-website
```

Move to this folder for all other commands.

### 3. Set it up

Run the following commands to see that *your local copy* has a reference to *your forked remote repository* in Github :octocat:

```sh
$ git remote -v
origin  https://github.com/<YOUR_USERNAME>/community-website.git (fetch)
origin  https://github.com/<YOUR_USERNAME>/community-website.git (push)
```

Now, lets add a reference to the original [community-website](https://github.com/we-developers-community/community-website) repository using

```sh
$ git remote add upstream https://github.com/we-developers-community/community-website.git
```

> This adds a new remote named ***upstream***.

See the changes using

```sh
$ git remote -v
origin    https://github.com/<YOUR_USERNAME>/community-website.git (fetch)
origin    https://github.com/<YOUR_USERNAME>/community-website.git (push)
upstream  https://github.com/we-developers-community/community-website.git (fetch)
upstream  https://github.com/we-developers-community/community-website.git (push)
```

### 4. Sync it

**Always keep your local copy of repository updated with the original repository.**
Before making any changes and/or in an appropriate interval, run the following commands *carefully* to update your local repository.

```sh
# Fetch all remote repositories and delete any deleted remote branches
$ git fetch --all --prune

# Switch to `master` branch
$ git checkout master

# Reset local `master` branch to match `upstream` repository's `master` branch
$ git reset --hard upstream/master

# Push changes to your forked `community-website` repo
$ git push origin master
```

### 5. You're Ready to Go

Once you have completed these steps, you are ready to start contributing by checking our Issues and creating [pull requests](https://github.com/we-developers-community/community-website/pulls).

### 6. Create a new branch

Whenever you are going to make contribution. Please create seperate branch using command and keep your `master` branch clean and most stable version of your project (i.e. synced with remote branch).

```sh
# It will create a new branch with name feature-<FEATURE YOU ARE WORKING ON> and switch to that branch
$ git checkout -b feature-<FEATURE YOU ARE WORKING ON>
#Example
#$ git checkout -b feature-eventsPage
```

Create a seperate branch for contibution and try to use same name of branch as of your contributing feature.

To switch to desired branch

```sh
# To switch from one branch to other
$ git checkout <BRANCH NAME>
#Example
#$ git checkout feature-eventsPage
```

To add the changes to the branch. Use

```sh
# To add all files to branch feature-<YOUR FEATURE>
$ git add .
```

Type in a message relevant for the code reveiwer using

```sh
# This message get associated with all files you have changed
$ git commit -m 'relevant message'
```

Now, Push your awesome work to your remote repository using

```sh
# To push your work to your remote repository
$ git push -u origin <BRANCH NAME>
#Example
#$ git push -u origin feature-<YOUR FEATURE>
```

Finally, go to your repository in browser and click on `compare and pull requests`.
Then add a title and description to your pull request that explains your precious effort.

## Guidelines

- Issues will be assigned on a first come, first serve basis. You just have to comment on the issue, asking to be assigned, and it will be done if found fit.
- Preferably, you cannot work on any issue that is not assigned to you.
- In case you want to submit an improvement to an existing feature or section, we prefer that you create an issue, describing in details your improvement. This will help others to analyze your contribution.
- If you have anything else in mind, create an issue and please wait for it to be assigned to you. You can then start working on it and create a PR.
- All PRs must be made from a Branch. Create a separate branch for every Issue you are working upon and once found fit, make a PR.
- If you have no idea what are issues or PRs, please do refer to this link

**Make sure your code works before submitting it :D**