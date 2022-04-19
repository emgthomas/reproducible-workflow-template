Emma Thomas & Matt Cefalu
12/15/2020

# Setup

This file provides basic directions on how to start a git repository for a new research project using this template as a starting point and push it to GitHub. Feel free to delete it after setup is complete.

First, create an empty repository (repo) on GitHub or other remote host. 
To do this on GitHub, go to github.com, login to your account, and click the 'New' icon (top left in green). Enter a short, descriptive name for your repository, choose public or private, and hit 'Create repository'.

Next, download a compressed version of this template (on GitHub, click the green 'Code' icon and select 'Download Zip'). 
Unzip the directory in the desired location on your local machine, and rename it. 
Navigate to this new directory in terminal (Mac/Linux) or command prompt (Windows). Initialize your new repo as follows:

    git init

Add the basic files from the template and commit these changes. Commiting the `.gitignore` file is *strongly recommended*, as this ensure that all versions of your repository will ignore the same files.

    git add *
    git add .gitignore
    git commit -m "<your message here>"

To connect your local repo to remote repo on GitHub, run the following commands:

    git remote add origin git@github.com:<your_username>/<repository_name>.git
    
Finally, push your new repo to GitHub:
    
    git push -u origin master

Now proceed to use git as normal.

**Note**: If you are working mainly on a remote server (e.g., pandora) and will not store the repo on your local machine, you may find it easiest to clone the template repository directly to the server. Then, clear the git files in order to start your new git repo using the command below, and initialize the new repo as above.

    rm -rf .git

# Basic git workflow

Here is a reminder about basic git commands and workflow.

First, make your new changes. When you are happy with your changes, you need to add the changed files and commit the changes. Commiting is like taking a "snapshot" of your repository in its current state, and the `add` command tells git which files you want to update in your snapshot.

To add a file such as `README.md`, use

    git add README.md 

It is generally considered best-practice to add files individually, but as a short-cut, you can add all changed files using:

    git add *
    
Next, commit changes using:

    git commit -m "<ADD INFORMATIVE MESSAGE ABOUT THE CHANGES YOU MADE>"

Finally, you should push your changes to GitHub:

    git push origin master

## Pulling changes

At the start of any work session, before making any new changes, it is advisable to first check if others have updated the repository by pulling changes from GitHub:

    git pull origin master
    
You can skip this step if you are the only person working on the repository.  

If you try to pull changes, and you get an error message like 

    error: Your local changes to the following files would be overwritten by merge

or

    Your branch is ahead of ‘origin/master’ by x commits

Don't worry; this just means that you need to resolve some conflicts between what is on GitHub and changes you have made locally.
