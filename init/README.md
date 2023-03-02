## How to initialization git repository   
* There are two-way to initialize git repository    
1. Using local machine.        
2. Using git repository.  
   
## Using local machine    
* Method 1
1. **git init -b branch_name**   
2. Create empty folder   
3. git status give branch name 

* Method 2
1. **git init**   
2. Create empty folder  
3. git status branch name is master

* Method 3
1. **git init folder_name  -b branch_name**  
2. Don't create a folder because git also create empty folder and initialize git repository.
3. It creates folder_name inside folder create github repository.  
4. Inside .git folder   

## Using github repository.   
* Method 1 
1. **git clone `https://github.com/MaazMS/versioncontrol.git`**      
2. It creates github repository on a local machine.    

* Method 2   
1. **git clone https://github.com/MaazMS/versioncontrol.git folder_name**   
2. It creates github repository on a local machine.  
3. It creates folder_name inside folder create github repository

## Inside .git folder
````  
ls -a
.  ..  .git
cd .git

tree
.
├── branches
├── config
├── description
├── HEAD
├── hooks
│   ├── applypatch-msg.sample
│   ├── commit-msg.sample
│   ├── fsmonitor-watchman.sample
│   ├── post-update.sample
│   ├── pre-applypatch.sample
│   ├── pre-commit.sample
│   ├── pre-merge-commit.sample
│   ├── prepare-commit-msg.sample
│   ├── pre-push.sample
│   ├── pre-rebase.sample
│   ├── pre-receive.sample
│   └── update.sample
├── info
│   └── exclude
├── objects
│   ├── info
│   └── pack
└── refs
    ├── heads
    └── tags

9 directories, 16 files
 ````    

## Create now repository  
1. If create a new repository without branch name it create on master branch.  
2. Also create a new repository with branch name.     
3. check branch name master and current branch by folder name command.  
4. `cd .git/` under `cat HEAD` show branch name.  
5. `git status`  it is also showed branch name.  
6. `git --show-c` also show a current branch.  
