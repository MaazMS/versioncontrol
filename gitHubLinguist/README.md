##  GitHub Linguist  
1. The files and directories within a repository determine the languages that make up the repository. With GitHub,      
   you can view a repository’s languages to get a quick overview of the repository.   
1.  GitHub uses the open source Linguist library to determine file languages for syntax highlighting and repository statistics.  
    Language statistics will update after you push changes to your default branch (which is usually master).  
1. GitHub Linguist is a library is used on GitHub.com to detect blob languages, ignore binary or vendor files,          
   suppress generated files in diffs, and generate language breakdown graphs.  
1. Basically, Linguist is a library that runs on every GitHub repository. It checks every file and directory and detects  
   the programming language used in that file.     
## How does Linguist work?  
1. Linguist takes the list of languages it knows from languages.yml and uses a number of methods to try to determine   
   the language used by each file, and the overall repository breakdown.  
1. The result of this analysis is used to produce the language stats bar which displays the languages percentages for    
   the files in the repository. The percentages are calculated based on the bytes of code for each language as reported    
   by the List Languages API.     
   
## How to fix common Linguist issues
1. My repository isn’t showing my language  
1. My repository is detected as a wrong language  
* solution 
1. Add a .gitattributes file to the root of your project    
    1. Using `linguist-language` attribute to override language extensions.    
    1. Using `linguist-documentation` attribute to mark or unmark paths as documentation.  
    1. Using the `linguist-vendored` attribute to vendor or un-vendor paths.  
    1. Using the `linguist-generated` attribute to mark or unmark paths as generated.  
    1. Using the `linguist-detectable` attribute to mark or unmark paths as detectable.  
    