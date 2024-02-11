### Git Assignment for DevOps Internship
-----------------

 1.Repository Setup:
   ---------------
   - The below image shows the repository forked from Seclists which is public repo available in the github. The fork feature allows us to create a copy of the original repo and operation can be done in it without impacting the original repo.
    
        
![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/1.1-fork%20repo.png)



  - The attached below snap display the remote repo which is in my github account been clone into my local machine using ssh git clone function.
     



![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/1.2-%20Clone-forked-repo-in-local.png)



   - To avoid left behind from original repository after multiple major changes in it, upstream is implemented to fetch and pull the changes if there is any.
     


![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/1.3-Upstream-to-Original-Rep.png)

     
2.Branching and Workflow:
-----------------
     
  The following image expose the creation of a branch called **develop** under master branch. For that 
                     ```
                     git branch develop
                     ```
       command is executed.


   ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/2.1-Develop-branch-create.png)


     
   - A simple script file called **lft-intern.js** is created inside feature/add-advanced-functionality and after that, it is staged and committed using `git add . && git commit -m`
       Upon opening the file lft-intern-js using `cat lft-intern.js`
       ```
            welcome to the leapfrog
            hi everyone
            welcome hai
            welcome everyone in leapfrog
            welcome everyone
            feature/add-advanced-functionality
            welcome guys feri ni
            helllllo
            hey man
       ```
       Then subsequently,
       ```
       git checkout develop
       git merge feature/add-advanced-functionality
       git checkout master
       git merge develop
       ```
  
       
       ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/2.2%7C2.3-feature%20branch%20and%20merge%20into%20develop.png)


    
     - A release branch called release/v1.0 is created and a tag which refers to the same commit is created.
  
        > `git tag -a 'v1.0' -m 'v1.0 version release'`
  
       ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/2.4%7C2.5-release%20branch%20and%20tag%20.png)

       
     - The branch later is merge into develop and master.
       
       ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/2.5-merge%20into%20master%20%26%20develop.png)

       
3.Conflict Resolution:
   ------------------
   - For simulating the merge conflict, a changes inside the file called lft-intern.js has been done and committed under **develop** branch and same line change was also performed inside **feature/add-advanced-functionality** branch and commit is executed, which after merging into the develop branch of changes into feature branch, a conflict occurs which led us to changes our conflicting file as desire. The resolve was done successfully after manually organizing the code which act for conflict in merge.
     
   **The conflicted file looks similar like**


```
       This is the feature branch.
    
        <<<<<<< HEAD
    
       This line is unique to the main branch.

        ===============================

        This line is unique to the feature branch.
    
       >>>>>>> feature/add-advanced-functionality

  ```
     
  - Head refers to contain changes from the current branch (in this case develop)
  - The '=========' refers separation between conflicting changes
  - The 'feature/add-advanced-functionality' contain changes from the brach being merged.
     
  ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/3.1-change%20in%20code%20line%20in%20feature%20-deliberate%20conflict.png)

  

   ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/3.1%7C3.2-change%20line%20of%20code%20in%20devlop%20branch%20and%20merge.png)
     
     
![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/3.2%7C%20resolve%20conflict%20manually%20editing%20conflict%20file.png)


     
4.Git Submodules:
   ------------------------
   Submodules are useful when the project require external libraries or codebase as part of project.
   The main command to add submodule is:
   `git add submodule https://github.com/user-account/repository`
   
![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/4.1%7CSubmodule%20point%20to%20another%20github%20repo.png)
   
   The added image below present extra information regarding the submodule project initialization and update to the latest remote.

   
  ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/4.2%7CReadme%20update%20with%20init%20and%20update.png)

     
5.Hooks and Custom Scripts:
   -------------------
   - The post-merge hook is one of the hook naming convention that trigger once the merge is successfully done. Hook need to be presented inside the .git/hooks/ directory. The created post-hook should be in executable state which is done using `chmod +x post-merge` for it to be executable.
  
     
 ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/5.1%7Cpost-merge%20naming%20hook%20create%20inside%20.git%3Ahooks.png)
     

   ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/5.1%7Csuccessful-merge-shell-script-create.png)
     
     
   - Here, the post-merge carry other executable file which needed to be in execution form. Once the post-merge got triggered, the bash code too get executed.

  
     ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/5.2%7Cset%20executable%20permission%20for%20script.png)
     
     
     ![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/5.2%7CSuccessful%20Merge.png)
     
     
6.Interactive Rebase:
   --------------------------
   The image below define using rebase for organizing the less significant by squashing them.
   The squashing is perform using 
` git rebase -i HEAD~3`
where
-i flag represent interactive mode where the squashing, picking and other features are performed.
HEAD points to the latest commit of the current branch
with HEAD~3, it means we want to squash the recent three commits.
While choosing pick and squash, we should always be aware that old recent commit should be set as Pick and other two recent must set as squash.


![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/6.1%7CRebase.png)


![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/6.1%7Crebase%20squash.png)


![welcome to nepal](https://github.com/LF-DevOps-Training/feb-8-git-assignments-binaya-baral-newpaney145/blob/main/materials/6.2%7CVerify%20rebase.png)

     
7.Documentation and README:
   ------------------------
   - Update the README with comprehensive instructions on the Git workflow used, including details about branching, submodule initialization, and any additional steps. 

*This assignment is designed to challenge participants with various Git scenarios commonly encountered in real-world development environments. Adjust it as needed to suit the specific focus areas of your DevOps internship*
