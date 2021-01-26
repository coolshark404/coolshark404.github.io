---
layout: post
title: Some problems i have to use git
date:  2021-01-27
tags: Linux
---

### Pull a old git repository in a new computer


`git init` 

`git pull YOUR_NEW_REPOSITORY` 

`git remote add origin YOUR_NEW_REPOSITORY` 

`git config --global user.email "USER_EMAIL"`  

`git config --global user.name "USER_NAME"`  

`git push --set-upstream origin master`  

### Repeat input password when your push git code


If we `git clone` to download by https instead of git@git(ssh) or `git push/pull`, git always hint us to input account/password, which make us disgust

Resolve:

`git bash` into your local repository and input

`git config --global credential.helper store`

after execute this command, it is auto product a txt file in which record your account and password

`git push` input the last password   

### Push error

Tips: refuse to update, because of not exist local commit included by remote repository

Reason: the repository you want to push was been used(remote add origin master..) by other local repository and see 'Git push --help to find more information'

Resolve:

1. force to push　　 

`git push -u origin +master`
　　　　　　　

2. download your remote repository to modify then commit
    
`git clone [your remoterepositiry page]`  

### error: pathspec 'modify' did not match any file(s) known to git

Resolve:

`$ git commit -a -m "modify"`  
