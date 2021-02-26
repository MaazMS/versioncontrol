## How to initialization git repository   
* There are two-way to initialize git repository    
1. Using local machine.        
1. Using git repository.  
   
## Using local machine    
* Method 1
1. Create empty folder   
1. **git init -b branch_name**   

* Method 2
1. Don't create a folder because git also crraete empty folder and initialize git repository.  
1. **git init folder_name  -b branch_name **    
1. It create folder_name inside folder create github repository.  
1. Inside .git folder   

## Using github repository.   
* Method 1 
1. **git clone `https://github.com/MaazMS/versioncontrol.git`**      
1. It create github repository on a local machine.    

* Method 2   
1. **git clone https://github.com/MaazMS/versioncontrol.git folder_name**   
1. It create github repository on a local machine.  
1. It create folder_name inside folder create github repository

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