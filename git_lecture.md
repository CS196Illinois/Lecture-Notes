# Git Lecture
Lecture on Git, Github, and using Git in Class

## What is Git?
Git is a VCS, or Version Control System. Version control is a system that records changes to a file or set of files over time so that
programmers working on a project have an archive of specific versions. Version Control is an essential part of software management
and is used ubiquitously in industry.

## Why use VCS/Git?
### Collaboration
Collaborating on a project is extremely complex without a Version Control System. This would be the equivalent of 
### Versioning
Keeping different versions of your project is essential, especially in industry. If you break build, you want to be able to roll back.
Versioning allows you to neatly store file states, commit logs, and diffs so that you can reason about your project temporally.
### Backups
Github stores your files on the cloud when you push. This means that your files, including all of the versioning information, is
safe.
### Logging and Issuing
Using a VCS such as Github makes it really easy to track issues, bugs, and manage how, where, and when code is written into the project.

## Basic Git
Git is a VCS. There are other VCS, such as SVN (which you will use in classes). Github is a service layer on top of Git. Github
is a tool that most open source and collaborative projects use when they want to use GIT VCS. Another popular example is Bitbucket.
Bitbucket and Git both use the Git VCS. This means that in terms of versioning and commands, Github and Bitbucket are exactly the same.
The tools that are built on top of Git though, are different.

### Initializating a Git "repo"
A single instance of Git is called a repository, or "repo". This repo keeps track of all of the files inside, as well as the
versioning information such as commit objects and references to commit objects, called "heads".

You spawn a git repo by typing the following command in the directory that you want to verson control.

```
$ git init
> Initialized empty git repository in yourFolder // 
```

This root directory is now called the "working directory". Git now tracks all changes and versions made to your working directory.

You have now intialized a git repo in your working directory, but you need to actually tell Git to take a snapshot of all the
files inside your repo. Git will not automatically save versions for you, you need to tell Git to take snapshats of your files
with commands.

The following command tells git to keep track of the file

```
$ git add .
```

Your files are now stored in a temporary staging area called the "index", which is used to hold all intermediary versions of your
Git repo in staging (in preparation to actually save).

You can now type the following command to permanently take a snapshot of your files and store it in Git

```
$ git commit
```

This command will prompt you for a commit message. Type in whatever you want. You now have stored a version of your project in Git.

Lets say you have 10 files in your project, file0, file1, file2.... file9. Lets say that you worked on file0, file1, and file2, and you want to commit to git.

Again, you first have to add your changed files to the staging environment.

```
$ git add file0 file1 file2
```

Now you can commit your changed files. Your computer now has a snapshot.
```
$ git commit -m "your commit message"
```

Now you have your files version controlled in your local machine, but you have to push to the cloud (Github) in order to share your progress with your teammates.
```
$ git push origin master
```

origin = remote
master = branch

If you want to download changes that your teammates have made in the cloud to your local version:
```
$ git pull origin master
```

If you want to add a new remote
```
$ git remote add origin https://github.com/user/repo.git
```

If you want to create another branch
```
$ git checkout -b "yourBranchName"
```

























