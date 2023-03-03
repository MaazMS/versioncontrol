## Remote repository   
1. A remote repository is github repository which is use remotely.   
2. It is used when one github repository work on a multiple developer all developer create a remote repository   
and changes to their remote repository it is not effected to github repository.    

## How to create remote repository  
1. **git clone URL**  
2. URL is github repository URL.
3. Example `git clone https://github.com/MaazMS/versioncontrol.git`  
4. It creates copy of project without effected the original repository.     

## How to give a new name to remote repository  
1. **git clone URL new_name_of_repo**
2. Every clone repository have name.  
3. How to change clone repository name for working as remote repository.   
4. Example `git clone https://github.com/MaazMS/versioncontrol.git  Git`    
5. It creates a remote repository with name Git.    

## Remote name  
1. **git remote add remote_name URL**
2. Once we clone  git repository  give default name `origin` to remote name.  
3. To add a remote name to clone repository to share information to each other.     
4. Example `git remote add r1 https://github.com/MaazMS/versioncontrol.git`

## Remote name rename   
1. **git remote rename old_remote_name  new_remote_name**
2. To change current remote name to give new name.    
3. It changes a remote name.    

## Delete remote name  
1. **git remote remove remote_name**
2. If you want to delete a remote name.   
3. It deletes a remote name.     

## Show a remote name and repository url  
1. **git remote -v**
2. How to show a remote name and a repository URL.  
3. It shows a remote name and a repository URL.