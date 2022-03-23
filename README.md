# Installation 

 Download the installer file from website: https://git-scm.com/downloads   
 Run the above downloaded file   


# Git local config

 git config --global user.name "xxx xxx"   
 git config --global user.email "xxx xxx"   


# SSH setup

 Run below commands in local   
 cmnd > ssh-keygen -o   
 cmnd > cd ~/.ssh   
 cmnd > cat id_dsa.pub   
 copy and add above key into your github account   

# Git Areas

 There are three main areas in git   
 The Working Tree : The Working Tree is the area where you are currently working   
 The Staging Area (Index) :The Staging Area is when git starts tracking and saving changes that occur in files (After git add .)   
 The Local Repository: Mainly what you will see in your Local Repository are all of your checkpoints or commits. (After git commit -m "msg")   

# setup new project

 cmnd > git init   
 cmnd > git add .   
 cmnd > git commit -m "commit msg"   
 create a repo in remote   
 cmnd > git remote add origin https://github.com/profile_name/repo_name.git   
 cmnd > git push -u origin branch_name   

# Branches 
List branches (the asterisk denotes the current branch)    
cmnd >  git branch	
List all branches (local and remote)  
cmnd > git branch -a	
Create a new branch   
git branch [branch name]	
Delete a branch in local      
cmnd >  git branch -d [branch name]	  
Delete a remote branch   
cmnd > git push origin --delete [branch name]  
Create a new branch and switch to it   
cmnd > git checkout -b [branch name]	  
Clone a remote branch and switch to it   
cmnd > git checkout -b [branch name] origin/[branch name]  
Rename a local branch   
cmnd > git branch -m [old branch name] [new branch name]   
Switch to a branch    
cmnd > git checkout [branch name]    
Switch to the branch last checked out   
cmnd > git checkout -       	
Merge a branch into the active branch   
cmnd > git merge [branch name]     
Merge a branch into a target branch     
cmnd > git merge [source branch] [target branch]    	
Stash changes in a dirty working directory    
cmnd > git stash	 
get stashed changes  
cmnd > git stash pop      
Remove all stashed entries   
cmnd > git stash clear	   