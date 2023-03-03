## What is the used of git push   
1. The git push command is used to upload local repository content to a remote repository.   
1. In other word update a remote repository using a local repository used git push.  

## Problem working on same branch  
1. **git status**
2. You are clone the repository.  
3. search a remote name, and a branch name.
4. Example   
```  
On branch branch_name
Your branch is up to date with 'origin/branch_name'.

nothing to commit, working tree clean
```  
1. create a new branch and work on a new branch because if you work on same branch and after that if push the code it shows.     
2. Example have branch_name = b1.     
```   
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: error: refusing to update checked out branch: refs/heads/b1
remote: error: By default, updating the current branch in a non-bare repository
remote: is denied, because it will make the index and work tree inconsistent
remote: with what you pushed, and will require 'git reset --hard' to match
remote: the work tree to HEAD.
remote: 
remote: You can set the 'receive.denyCurrentBranch' configuration variable
remote: to 'ignore' or 'warn' in the remote repository to allow pushing into
remote: its current branch; however, this is not recommended unless you
remote: arranged to update its work tree to match what you pushed in some
remote: other way.
remote: 
remote: To squelch this message and still keep the default behaviour, set
remote: 'receive.denyCurrentBranch' configuration variable to 'refuse'.
To /home/maaz/github/Git/versioncontrol/test/p
 ! [remote rejected] b1 -> b1 (branch is currently checked out)
error: failed to push some refs to '/home/maaz/github/Git/versioncontrol/test/p'
``` 
1. central repository branch name **b1** and not create a new branch in a remote repository.  
2. There for a remote repository branch name is also b1.   

## How to push remote code to central repository   
1. First create a new branch.  
2. writing some code.  
3. push the code.  
4. `git push remote_name branch_name`   
5. `git remote -v` check a remote name.    
6. `git branch -all` check branch name.  
7. Example have new branch_name = b2    
```  
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 400 bytes | 400.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
To /home/maaz/github/Git/versioncontrol/test/p
 * [new branch]      b2 -> b2
```