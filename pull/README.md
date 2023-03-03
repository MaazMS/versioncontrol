## Why use git pull   
1. It is used to update a remote repository.  
2. It means if the central repository have any change a then remote repository is updated by git pull.     

## Master branch changes update remote master    
1. **git pull origin master**
2. The central repository change something.   
3. To update remote repository.      
4. Example    
5. Open remote branch
6. Go to mater branch, It shows some message.  
```   
git checkout master 
Switched to branch 'master'
Your branch is behind 'origin/master' by 1 commit, and can be fast-forwarded.
  (use "git pull" to update your local branch)
```
1. Update remote   
```   
git pull origin master
From /home/maaz/github/Git/versioncontrol/test/b1
 * branch            master     -> FETCH_HEAD
Updating 19ac306..ad02adc
Fast-forward
 b.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
```
````   
From /home/maaz/github/Git/versioncontrol/test/p
 * branch            master     -> FETCH_HEAD
Already up to date.
````  

## Remote branch changes by central repository     
1. Create a new branch and push to central repository.    
2. A central repository is switch to remote branch.  
3. Update the file which is push by a remote branch.   
4. Again switch to master branch.   
5. GO to remote repository and do something and push to central repository.   
6. It shows here b2 is branch name.    
````   
! [rejected]        b2 -> b2 (fetch first)
error: failed to push some refs to '/home/maaz/github/Git/versioncontrol/test/b1'
````  
1. **git pull origin b2**
2. It means first update a remote repository.    
3. It shows conflict because same file and same line have changes by a central repository.  
````   
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 258 bytes | 258.00 KiB/s, done.
From /home/maaz/github/Git/versioncontrol/test/b1
 * branch            b2         -> FETCH_HEAD
   58f6f84..f3d2034  b2         -> origin/b2
Auto-merging b1.txt
CONFLICT (content): Merge conflict in b1.txt
Automatic merge failed; fix conflicts and then commit the result.
```` 
1. **git push origin b2**
2. Solve merge means to edit file. what you want and what you don't want.  
3. Then git push.  
