## git add  
1. **git add file_name_or_folder_name** 
2. To add file and folder use git add command 
3. It stores file staging area.  
4. Review the changes in staging area using command **git status** and status are modified, deleted, or added.  
5. ![](https://res.cloudinary.com/practicaldev/image/fetch/s--Si7ksd-d--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://cdn-images-1.medium.com/max/800/1%2AdiRLm1S5hkVoh5qeArND0Q.png)   
 
## git commit   
1. **git commit -m "message"**   
2. **git commit -am "message"** or **git commit -a -m "message"**  
3. After git add commit.
4. `-m` for message.   
5. `-a` for push all the files and folder that are showing modified, deleted.  
6. Example  
```Example 
$ git status 
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
        modified:   gitstach/README.md
        
$ git commit -am "command add and commit used "
[master 545a83d] command add and commit used
 3 files changed, 18 insertions(+), 52 deletions(-)
 rewrite README.md (98%)

$ git status 
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

```