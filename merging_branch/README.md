## Merging branch   
1. Merging is used to merge the code.  
1. git is provided auto conflict feature to merge the code.   
1. git auto conflict feature failed is some case.  
1. example Change the same line and same file for master branch as well as new branch.  
1. Then use merge give conflict which is solved manually.   

## merge without conflict     
1. first move to master branch.  
1. **git merge branch_name**   
* example   
```   
git merge b2
Updating 5f34ded..1647084
Fast-forward
 b.txt | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

```  
## merge with conflict    
1. change on same file and same line give conflict which is not solved by git.   
* example.   
1. touch b.txt   
1. nano b.txt write the file example 1   
1. git add and commit b.txt file.   
1. create a new branch.    
1. touch b.txt
1. nano b.txt write the file example 1
1. git add and commit b.txt file.     
1. **move to master branch**  
1. `git merge branch_name`      
1. when perform merging it show. 
```   
Auto-merging b.txt
CONFLICT (content): Merge conflict in b.txt
Automatic merge failed; fix conflicts and then commit the result.   
```  
1. cat b.txt    
```  
<<<<<<< HEAD
1
=======
2
>>>>>>> b2 
```  
1. `<<<<<<<` HEAD show master branch    
1. `>>>>>>>` It shows a new branch with their name b2.     
1. `=======`  It creates difference between branches.      
1. developer is chosen correct and useful.   
1. git add and commit b.txt file.  




