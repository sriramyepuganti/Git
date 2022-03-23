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
To pick particluar commit   
git cherry-pick commit_id    

# Trach changes 

Track the changes that have not been staged   
cmnd > git diff    
Track the changes that have been staged but not commited   
cmnd > git diff --staged    
Track the changes after commiting  
cmnd > git diff Head  
To check state of working directory and staging area  
cmnd > git status  
To display Show object   
cmnd > git show   

# commit history

logs  
cmnd > git log  
to check author of the code   
git blame file_name  
# sharing and updating

sync up with remote  
cmnd > git fetch master (changes will not be visible in pwd)   
To see the above changes   
cmnd > git diff master origin/master  
To get the changes into pwd   
cmnd> git merge   
Pull changes from remote repository (pull = fetch + merge)   
cmnd > git pull origin [branch name]	
Push a branch to your remote repository     
cmnd > git push origin [branch name]	 
Push changes to remote repository (and remember the branch)   
cmnd > git push -u origin [branch name]	   
Push changes to remote repository (remembered branch)  
cmnd > git push    	    
Update local repository to the newest commit (remembered branch)       
cmnd > git pull    	
Upstream and downstream   
cmnd > git remote -v   
cmnd > git push --set-upstream origin master   
rebase with latest commit   
cmnd > git rebase branch_name  
 
# Tags

Git has the ability to tag specific points in a repository’s history as being important. Typically, people use this functionality to mark release points    

Git supports two types of tags: lightweight and annotated.    

A lightweight tag is very much like a branch that doesn’t change — it’s just a pointer to a specific commit.    
cmnd > git tag v1.0.0   

Annotated tags, however, are stored as full objects in the Git database.   

cmnd > git tag -a v1.0.0 -m "msg"   

show tag details   
cmnd > git show tag_name   

push tag details  
cmnd > git push origin tag_name    


# undo changes

In Pwd:    
cmnd > git checkout file_name  
cmnd > git stash   
cmnd > git reset --hard (reset permanently) 
In staging :  

To discard all local changes. but save them for later  
cmnd > git stash   
To unstage but keep change   
cmnd > git restore --staged file_name  
To unsatge everything, but keep your changes    
cmnd > git reset   
unstage the file to current commit   
cmnd > git reset HEAD file_name   
discard everyting permanently   
cmnd > git reset --hard  

In local repo:   

cmnd > git reset HEAD~1 (will remove one commit and changes will be in pwd)   
cmnd > git reset --soft (will keep changes in staging area)  
cmnd > git reset --hard (will remove all changes)  

In remote:  

cmnd> git revert commit_id
