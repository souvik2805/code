### Git
##### 1. Goto CWD and type git status to check is it a Git repository or Not
-

 ```
>>>git status
fatal: not a git repository (or any of the parent directories): .git
```
-->Means it not a git repository

##### 2.  To make it git repository type git init
-
 ```
>>>git init

Initialized empty Git repository in C:/Users/BISWAS/Desktop/python/test/.git/
-->Means now this CWD become Git repository(now a .git hidden folder also created)

>>>git status

On branch master
No commits yet
Untracked files:
  (use "git add <file>..." to include in what will be committed)
```


##### 3.Insert all file in Staging Area
-

 ```
>>>git add --a
>>>git status
On branch master
No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
```

##### 4. To commit type git commit -m m means message
-
 ```
>>>git commit -m "Initial Commit"
>>>git status
On branch master
nothing to commit, working tree clean
```
##### 5. To see the commit message and the user use git log 
-
 ```
>>> git log
```
-->Here Head in the bracket use to indicate the last commit

##### 6.After working many file. check the git status. but If you want to stage a single file use
-
 ```
>>>git add <filename with extension>
>>>git commit -m "Change First.text and commit 3 "
>>>git log
```

##### 7.To delete git
-
 ```
>>>rm -rf .git
```
-->Very danger command

##### 8.To clone a repository for github use git clone. 
-
 ```
>>>git clone <url>
or 
>>>git clone <url> <custom-folder-name>
```

##### 9. Use q to exit .

##### 10. To add single file in statge
-
 ```
>>>git add <filename>
```
##### 11.  Git ignore->Create a folder .gitignore
-
 ```
>>>touch .gitignore
```

##### 12.  Add all the file in .gitignore to ignore the file.
-
 ```
>>>git status
>>>git add .
```

##### 13.  You can also ignore a particulary type file usig *.log in .gitignore file.
TO ignore a whole directory use <directory name>/
-

##### 14.   Compare the working status and the Git staging area.
-
 ```
>>>git diff
```

##### 15.   Compare the working status and the Git staging area.
-
 ```
git diff --staged
```

##### 16.   Direct commit without the Staged Step ----------------------->
-
 ```
>>>git commit -a -m "This is direct commit"
```

##### 17. To delete a file using bash or rename
-
 ```
>>>git rm <filename>
>>>git mv <filename> <re-namefile>
```
##### 18. To Ignore a File which is previously track but now we do't want to track then add the file name of .gitignore file and run git explictly untrack command
-
 ```
>>>git rm --cached <filename>
```

##### 19.  Use git log -p to see log along with the changes
-
 ```
>>>git log -p
>>>git log -p -2

-->to see only 2 log

>>>git log --stat

>>>git log --pretty=oneline

>>>git log --pretty=short

>>>git log  --pretty=full

>>>git log --since=2.days

>>>git log --since=2.weeks

>>>git log --since=2.months

>>>git log --since=2.years

>>>git log --pretty=format:"%h -- %an"

```

##### 20. ________What to add new stage file to the existing commit(Last Commit) --means add the changes to the Last commit not create a new commit and also the commit message
  -
  
  ```
  >>>git commit --amend
  ```
  - It will open vim editor first click E to read. 
Then Press <i> button to edit
then press <esc> button
then press <:> the <qw> to quit and save  the Vim

#####   21.For unstage the file use
-
```
 >>>git restore --staged <filename>
```
>>>git restore --staged <filename>

#####   22.To get back the Last commit file data use
-
```
 >>>git checkout --<filename>
```

#####   23. To get back to Last Commit all the Files
-
```
 >>>git checkout -f
```
-->get back all the file

#####  24.  How to upload code
-
```
>>>git remote add origin <url>

-->git remote add -this fixed after that you can name it as source or anything here is origin

>>>git remote -v
>>>git push -u orgin master
```

#####  25. remote origin 
-
```
git remote rm origin
git remote add origin git@github.com:username/myapp.git
```
#####  26. Permission Denied------------------------------------------------->
-
```
i>>>ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

-->this for creating new key. Press y in Overwrite

ii>>>eval $(ssh-agent -s)

-->To see that the agent key is runing or not.

iii>>>ssh-add ~/.ssh/id_rsa

Identity added: /c/Users/BISWAS/.ssh/id_rsa (souvik2805@gmail.com)

iv>>>clip < ~/.ssh/id_rsa.pub 

or 
iv>>>tail < ~/.ssh/id_rsa.pub

-->in Clip the key  automatically copy. but in tail we have to manually copy it.
after that you have to create the ssh key in profile setting;
```

#####  26.
-
```
>>>git config --global alias.st status
>>>git config --global alias.unstage 'restore --staged --'
```

#####  26.
-
```
>>>git config --global alias.st status
>>>git config --global alias.unstage 'restore --staged --'
```
##### 27.-------------------------Creating and Switching Branches--------------->

```
>>>git checkout -b "branchename"
->This command will create a new branch and also switch to this new branch.
>>>git checkout master
>>>git branch
->To see the all the branch
```

##### 28. To merge go to master

```
>>> git merge <branch_name>
```

##### 29.  T0 get back to a particular Commit ----------------------->

```
>>>git checkout <identifier number> <filename>
```
-->This command will bring back the old file to CWD






