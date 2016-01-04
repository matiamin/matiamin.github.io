---
layout: post
title: "Git Basics: A Quick Reference"
excerpt: "Most common git commands to manage changes to your files."
tags: [sample post, images, test]
comments: true
---

> Git is a widely used version control system `(VCS)` that allows developers to manage changes to their own files and collaborate with others. It has become an essential tool for managing large scale projects.

This post is designed to give a brief overview of the most common `git` commands. If nothing else, it should serve as a quick reference. Practice makes perfect. The best way to learn is to actually execute the below commands on your computer as you go along, at least that is how I learn.

#### Installation
To get started, you will need a working Git installation. You can download it <a href="http://git-scm.com/" target="_blank">here</a>.

Open a new command prompt and run `git --version`. It should output the git version you just downloaded, the latest one being `git version 2.6.4`.

#### Basics
Below is all you need to start using Git to manage your own small projects and files.

* Create a Git repository in the current folder
* View status of each file in a repository
* Stage new changes for commit
* Commit the staged changes along a descriptive message
* View commit history

{% highlight html %}
git init
git status
git add <file>
git commit -m "descriptive message"
git log
{% endhighlight %}

#### Undo Changes
A `VCS` is useless if it cannot undo committed and untracked changes to to a file or project.

* View a previous commit
* Undo a commit by applying a new commit
* Delete untracked files
* Reset to match the most recent commit without staging the tracked changes for a commit
* Permanently undo uncommitted changes

{% highlight html %}
git checkout <commit-id>
git revert <commit-id>
git clean -f
git reset --hard
git reset --hard/git clean -f
{% endhighlight %}

#### Branches
In Git, a `branch` is an independent line of development, which allows developers to experiment with their own projects and collaborate with others.

* Create a new branch using the current directory as its base
* Navigate to a branch
* Merge a branch into the current (checked-out) branch
* Delete a branch. Note: checkout into separate branch in order to delete a specified branch
* Show all branches

{% highlight html %}
git branch <branch-name>
git checkout <branch-name>
git merge <branch-name>
git branch -d <branch-name>
git branch
{% endhighlight %}

#### Remotes
A Git remote repository lives on a server. It could be your repository or someone else's. You can push changes to it as well as pull changes from it to update your local repository.

* Create a copy of a remote Git repository in your local machine
* List all remote repositories
* Add a remote repository to your Git repository
* Once added, download information from the remote branch without merging anything
* Merge a remote branch into the checked-out branch
* Show all remote branches

{% highlight html %}
git clone <remote-path>
git remote
git remote add <remote-name>
git fetch <remote-name>
git merge <remote-name>
git branch -r
{% endhighlight %}

There is a lot more to Git. Again, this post is merely to serve as a quick reference
