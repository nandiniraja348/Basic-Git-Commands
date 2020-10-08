# Basic Git Commands

This repository contains all the basic git commands to start off with Git. 
It teaches you from very beginning how to set up a repository 
and make a push from your local to the remote.

I shall share you the process as to how this repository is created from beginning 

1. In your local, create a directory using the following command

        mkdir Basic-Git-Commands

2. Enter into the directory using (the change directory command)
         
        cd Basic-Git-Commands
      
3. Initialise the directory with a git command

        git init 
        
Now when you type in `ls -a` you will be able to find a `.git` directory, 
within which you will have all the configuration and the hooks like pre-commit 
necessary to perform certain operations when a git command is executed.

After executing the previous command, 
we will have a return statement stating `Initialized empty Git repository in <path of the local git repo/.git>`

Once initializing is done create a file named `README.md` using the command:

        vi README.md
        
Add the required content, in this case the readme file this file you are reading.

### IN GITHUB

1. Go to the repositories and create a new repo with the same name as the directory created in the terminal(This is a good practice. Else we might tend to confuse with the name of the Repo and the directory in our local).
2. Choose the owner to be your github repo/ where you want the new repo to be created.
3. Type in the name as `Basic-Git-Commands`.
4. Give a small description if you want about the repo. 
5. Choose either the repo has to be public/ private. 
If you want the repo to be visible for community people to look into and contribute make it `public`. 
Else if you feel it is a repo that you are going to create within your organisation/ personal work choose `private`.
6. You can either add the README.md and .gitignore files by ticking in the check box. 
As we are going to make a push from the terminal(in the local). Let's not select any.
7. Then click Create Repository

Having created a repo is set up at the remote git now, we will have to establish some connection between the local and the remote to fetch files from local.

Now we can stage our local changes to the git by using

        git add README.md

To see what all changes can be commited to the git use the command

        git status
        
Now you can see the changes ready to be commited. If you have any untracked files(files which are not added), Add it using the previous command if you want the untracked files also to be commited.

Commit the file with a readable message. The commit message has to convey the meaning of the commit for people who simulatenouly work on your project to understand what changes the project has undergone.

        git commit -m "Added the README.md file that states all the git commands and ways to setup git in local"

Check out `git log` - This shows the complete details of the commit. The changes that it shows are commit hash, the branch, the person who has commited, the date of the commit and the commit message. You can get out of the git log by typing in `q`

Next step is to choose the branch to which we are going to push the files to. Initially let's work with master. Using the following command set the branch to the master.

        git branch -M master
    
To push we will have to set the local to a remote path to push the changes to a particular repo(the repo's url can be found out from the Github, Choose Code in the repo -> take the URL from the HTTPS). This can be done using 

        git remote add origin https://github.com/<your_github_profile_name>/Basic-Git-Commands.git
     
After all these are successfully done. Run

        git push -u origin master
        
The changes are successfully pushed to the remote repo. Go to Github and check that the file has dropped in.


# GIT PULL


Made a change to check how the git pull --rebase works

