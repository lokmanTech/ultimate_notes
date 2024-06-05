# Git - Tracking your stuff!

### What is Git
Git is a free and open-source distributed version control system for tracking changes in source code over time during the various phases of software development. It coordinates work among programmers who work collaboratively during software development.

### Why use Git
- Tracks every change made to a file, making it easier to revert to any specific version.
- Keeps project history organized and well documented, allowing to track who made changes.
- Makes collaboration easier irrespective of the developers’ location.
- Maintain the original codebase while working on additional features.

### Git v. GitHub: Not the same Thing!
Think of Git as the tool that creates the timeline but doesn’t store your files online. That’s where GitHub comes in. GitHub is a popular online platform designed specifically for Git repositories. Imagine Git as a personal filing system and GitHub as a secure online storage locker for your versions.

### The Stages in Git
<p align="center"><img source="img/GitStages.png></p>

- Working Directory: This is the area where you create, modify, or delete your files for your project.
- Staging Area: This is the pre-commit area. Whenever a file is marked for commit it is moved to this area.
- Local Repository: This is where Git stores the committed changes. Upon commit, the changes made to the files in the staging area are saved permanently.

At any given point in time, every file will be in one of these stages.

### Installing Git

Download Git from the [official website](https://git-scm.com/downloads) and complete the installation.

After the installation, launch cmd, type the command `git --version`, and hit enter. You should be able to see the installed version of git.


### Initializing a Git repository

Create a new folder(this will be our working directory) with the name of your choice. Move into the folder and run the below command:

```md
git init
```

This will initialize a git repository(.git folder) in the current folder.
A repository tracks all changes made to files in your project over time and holds the configurations and other details related to the project.

### Configuring username and password

```md
git config --global user.name "Your name"
git config -global user.email "Your email id"
```

This will configure the user name and email at the user level for all the repositories.
You can omit the `--global` flag if you want to configure the user name and email for only the current repository. Configuring it at the system level is also possible using the `--system` flag (this might require admin/sudo access).
The name and email at the repository level have the highest precedence followed by the config at the user level and then at the system level.

To verify the details:

```md
git config user.name
git config user.email
```

This will print the username and password applicable to the current repository.

### The States in Git

- Untracked: You have created a new file that has not been committed yet.
- Modified: You have made changes to a previously committed file.
- Staged: You have marked the modified or created file for committing.
- Committed: You have successfully saved the files as a snapshot in your local repository.

<a align="center" source="img/StatesInGit.png></a>

You can check the status of files using the command:

```md
git status
```

This will show the current branch(master by default) and the status of files grouped as modified(or deleted), untracked, and staged.

### Branches in Git

The branches provide developers with separate workspaces for their code to work simultaneously without messing up the main line. This enables developers to create a new branch for a feature development or a bug fix for encapsulating their changes without affecting the main branch. There will be a main line of branch for project, typically named the “master” branch from which several branches diverge.

<a align="center" source="img/BranchingInGit.png></a>

### Getting Started

Let’s start by creating a new file and adding some content to it.

To do it from the command line we can use the command `echo content > filename.` For eg. `echo “Introduction to Git” > a.txt`.

After this, if you check the status you will see that file as untracked.

### Staging a file

To stage a file in your working directory:

```md
git add <file-to-stage>
```

To add all the files to staging:

```md
git add .
```

This will recursively stage all the files in the current directory and subdirectories.

### Unstaging a file

To unstage a file that you might have accidentally staged for committing, you can use the below command:

```md
git reset <file-to-unstage>
```

### Committing a file

A commit records changes to one or more files in your project by keeping a snapshot of the changes made over time. Each commit stores the changes made to the files since the previous commit.

To commit the files in the staging area use the command:

```md
git commit -m "commit message"
```

The -m flag stands for the commit message. Here you should describe in short the changes you have done in this commit which could be creating a file or a method, a bug fix, or any changes you would have made. It is a good practice to write in detail about what you have done. Now if you check the git status there will be nothing in there.

Change the contents of the last committed file and save it. And now if you check the git status you will see the status of the file as modified. This is because the contents of the file in the local repository snapshot and the file in your working directory do not match since you modified the file after you committed.

If you have been following the steps till now, go ahead and stage the file then commit the changes. This will be good practice for the steps we did till now.

### Viewing the commit history

You can view a summary of the git commit history using the command:

```md
git log
```

This will mainly show the commit id, author details, date, and time along with the commit message.
If are interested only in viewing the shorter version of the log with the id and the commit messages you can pass an additional --oneline flag.


### Working with remote repositories

To share your code with other developers you need to add your code to a remote repository.
For this, we will be using GitHub. If you don’t have an account sign up or if you do have an account then log in and create a new repository.

### Creating a remote repository on GitHub

After you log in, in the top right you will find a plus button, click on it then click on New Repository.

Give the repository a name of your choice. Scroll down and then click on the Create Repository button.

### Adding a remote repository

You can get the repository url of the newly created GitHub repository from:

<a align="center" source="img/GitRepo.png></a>

To add a remote repository to your local repository use the command:

```md
git remote add <remote-name> <repository-url>
```

Using this as our reference the command becomes git remote add github-repo https://github.com/amalsebs/GitPractice.git where ‘github-repo’ is our remote name and ‘https://github.com/amalsebs/GitPractice.git’ is our remote repository url.


To view the configured remote repositories we will use the command:

### Pushing to a remote repository

To push a specific branch of our local repository to the remote repository we will use the command:

```md
git push <remote> <branch-name>
```

Using this as the reference our command becomes git push github-repo master since we will be on the master branch by default. After pushing go to your repository in GitHub and you should be able to find your files there.

### Creating a local copy of a remote repository

Suppose you share the url of your public repository and your friend wants to start working on the repository. He should first create a local copy of a remote repository. To create a local copy of a remote repository:

```md
git clone <repository-url>
```

This will create a folder with the same name as the repository. After which it will create a .git folder and download the files in the repository to the folder.
To get the repository url from GitHub. This local repository will automatically be linked to the remote repository upon cloning.
Note: If you check the remote name here it will be origin which is the default value for the remote name.

### Update local repository from remote repository

Suppose your friend had committed new files from their system and pushed them to your remote repo. Now you want those changes to be updated in your local repository. To do this you will use the command:

```md
git fetch
```

This will fetch all the changes including the commits and branches from the remote repository and bring it to your local repository but not into the working directory.

### Update the working directory from the local repository

After fetching, the changes will be saved in the repo into a branch denoted by <remote>/<branch-name>. To bring these changes into our working directory we will need to perform a merge operation.

```md
git merge <remote>/<branch-name>
```

Using this as the reference our command becomes git merge github-repo/master.

### Update the working directory directly from the remote repository

```md
git pull <remote> <branch>
```

Using this as the reference our command becomes git pull github-repo master. This will get all the changes in the remote repository and bring it into our current working directory.
This command is a combination of fetch and merge operations.


### Git Workflow

<a align="center"><img source="img/GitWorkflow.png></a>





















