## Create branch   
1. **git branch branch_name**   
2. It creates a new branch for github repository.    

## switch branch   
1. **git checkout branch_name**   
2. it switches to new branch.    

##  All in one command create and switch branch  
1. **git checkout -b branch_name**   
2. `-b` for a branch_name.   
3. It creates a new branch.     
4. it switches to new branch.  

## Delete branch  
1. **git branch -D branch_name**  
2. `-D` for delete.  
3. It delete branch.   
4. `error: Cannot delete branch`  
5. Because you in a current branch.  
6. switch branch and delete branch.   

## Show branch   
1. **git branch**  
2. It shows all branches for current github repository.     

* Note : when create new branches in a local repository and enter **git branch** it not shows branches and their name.   
* solution once we create a branch locally use **git add** and **git commit** to add and commit some things after branches   
name show.