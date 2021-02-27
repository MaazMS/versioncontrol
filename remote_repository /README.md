## Remote repository   
1. A remote repository is github repository which is use remotely.   
1. It is used when one github repository work on a multiple developer all developer create a remote repository   
and changes to their remote repository it is not effected to github repository.    


## How to create remote repository  
1. `git clone url`  
1. url is github repository url.
1. example `git clone https://github.com/MaazMS/versioncontrol.git`  
1. It creates copy of project without effected the original repository.  

## Remote name  
1. Once we clone  git repository  give default name `origin` to remote name.  
1. To add a remote name to clone repository to share information to each other.    
1. `git remote add remote_name url`    
1. example `git remote add r1 https://github.com/MaazMS/versioncontrol.git`

## Remote name rename   
1. To change current remote name to give new name.   
1. `git remote rename old_remote_name  new_remote_name`   
1. It changes a remote name.    

## Delete remote name  
1. If you want to delete a remote name.  
1. `git remote remove remote_name `   
1. It deletes a remote name.     

## Show a remote name and repository url  
1. How to show a remote name and a repository url.  
1. `git remote -v`  
1. It shows a remote name and a repository url.