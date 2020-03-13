---
layout: post
title: GIT CLI CRASH COURSE
postimg: /assets/uploads/screenshot_20200307-002316.png
date: 2020-03-06T18:13:16.380Z
author: iamharsh
categories: [crash_course,git]
---
Hey folks, out there we all know about github and it is basically a git hosting site so now you must be wondering what is git? In simple words Git is a distributed version-control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files.

So now we must step further diving into git commands (GUI guys please stay away from this post).

## 1.git init
**Utility**: To initialise a git repo on your local machine in your current project directory.

## 2.git clone <url>
**Utility**: This command is use to clone a git repo on to your local machine this could be your own repo hosted on GitHub or any other repo by some other cool developer just like me. Here you just have to replace <url> with the url of that repo you want to clone or download.

## 3.git config
**Utility**: To config the git on your machine (mandatory) .
**Syntax**:

{% highlight bash %}
git config --global user.name "theuitown"
git config --global user.email "electronlabsdev@gmail.com"
{% endhighlight %}

## 4.git add
**Utility**: To save or add the changes you have made to the working directory this will not really take effect until you commit the changes.
**Syntax:**
{% highlight bash %}
"git add <file_name>" or "git add ." (to add all the files to repo)
{% endhighlight %}

## 5.git status
**Utility**: To check the status of the repo like what all changes you have made and what is added to repo and what not.

## 6.git commit
**Utility**: To commits / save the snapshot to the project history.
**Syntax**:
```git commit -m "add_any_commit_message"```

## 7. git stash
**Utility**: Temporarily save uncommited file into stash. So we can work on something else.

## 8. git diff
**Utility**: To see the details of changes you made to files.

## 9.git logs
**Utility**: This will show all of the commits you have made into the repo and other details about that commit and this basically shows you the history of your repo.

## 10.git revert
**Utility**: As the name suggests this command can revert the changes to last commit made incase something went wrong.
**Syntax** :
```
"git revert <commit-id>"
```
Here enter the commit id you can get it by git logs command.

## 11.git branch
**Utility** : It will list out all of the branches.
**Syntax**:```"git branch" or "git branch -a"``` to list remote branches as well.


## 12.git checkout
**Utility** : To switch between different branches.

**Syntax**:```
 "git checkout <branch name>" or "git checkout -b <branch name>"``` if you want to create a new branch and switch to it.


## 13.git push/pull
**Utility**: Push or Pull your changes to remote. If you have added and committed your changes and you want to push them. Or if your remote has updated and you want those latest changes.

**Syntax** :
```
"git pull <:remote:> <:branch:>" and "git push <:remote:> <:branch:>"
```

## 14.git remote
**Utility**: To check what remote/ source you have or incase you wanna add a new remote.

**Syntax**:
```
 "git remote" // to check and list. And "git remote add <:remote_url:>"
```

At the end i just wanna say that try it of yourself and once you have learned how to use git now you have the superpowers.

## *Peace out i will catch you in my next one.*
