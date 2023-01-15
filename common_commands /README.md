## git add  
1. TO add file in git use `git add file_name_or_folder_name`  
1. It stores file staging area.  
1. ![](https://res.cloudinary.com/practicaldev/image/fetch/s--Si7ksd-d--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/800/1%2AdiRLm1S5hkVoh5qeArND0Q.png)   

## git commit   
1. After git add commit.  
1. `git commit -m "message"`  
1. `-m` for message.   

## How to create a username and email for git  
1. git config --global user.name "username"  
1. git config --global user.email "email"   
* Linux os save email and password follow  Three command user.name, user.email  credential.helper .    
1. git config --global credential.helper store   

## How to check git log  
1. git log contain unique commit id, Author name, Date day month date time, message.  
1. `git log`   

## check status  
1. It shows branch name.  
1. It shows new files and staging area files.   

## git diff file1 file2  
1. Check difference between two files.   
1. `git diff commit_id1 commit_id2`  
1. commit_id1 is file 1 commit id.  
1. commit_id2 is file 2 commit id.   

## How to create gitignore   
1. gitignore file is ignore a file not add to github.   
1. `touch .gitignore`   
1. `git add .gitignore`  
1. `git commit -m "message"`   

## How to delete file in github 
1. git rm file_name 