Hello @everyone, welcome to our **Python Fast API and Docker BootCamp Day 1** ,  We usually starts our boot camp by learning, Git and GitHub here is what you are suppose to at least look at on day 1 👇🏻: 

Day 1: Introduction to Python, Git and Github. 

What you are expected to learn on Day 1:
* Introduction to Python for Web Development
* Learn how to create a “repository” (project) with a git hosting tool (like GitHub or Bitbucket)
* Learn how to copy/clone the repository to your local machine
* Learn how to add a file to your local repo and “commit” (save) the changes
* Learn how to “Push” your changes to your master branch
* Learn how to make a change to your file with a git hosting tool and commit
* Learn how to “Pull” the changes to your local machine
* Learn how to create a “branch” (version), make a change, commit the change
* Learn how to open a “pull request”.
* Learn how to “Merge” your branch to the master branch 

References 👇🏻: 

Few announcements for those who didn’t join the onboarding session on Saturday:
To get the certificate of completion you have to at least complete the first week of the boot camp and track your progress in these google forms :point_right::skin-tone-2: https://forms.gle/1TvMYRMvo3CrNkaN7, that is today, Monday to Friday, write and submit at least one technical article on a topic which will be given out tomorrow. 

Your article should be in one of the following topics: 
          1). Getting Started with Fast API and Docker. 
          2). Ultimate Docker and Fast API Guide 
          3). Fast API and Docker Play Book  
          4). Fast API and Docker CheatSheet 

We will be having two classes per week 8:00PM to 9:45PM EAT on Tuesday and Fridays. 

Important Link: 
          1). WhatsApp peer group :point_right::skin-tone-2: https://chat.whatsapp.com/H0wo1lrkufv8y1qbGXnIoK
          2). Slack channel invite link :point_right::skin-tone-2: https://join.slack.com/t/luxtechacademy/shared_invite/zt-wyrywawn-ImHODjmMeXvqa3ZUs5S8xg 

Every evening we will be sharing  reference materials and  you can join our 20 minutes  quick  catch up meeting everyday at 8:00 PM we will be using the same link we used on Saturday.  All the best, may your smart hard work pay

After the two weeks of learning, there will be a capstone project that you have to create in 5 days, and the best 5  projects gets a give away from Lux Academy and Data Science East Africa while the best project gets a giveaway + a boot paperback.


Python Tutorials: 


### **Git and GitHub Basics:**
Git is a version control system which comes handy when you're writing code as a team or independently. Some features that git allows includes; creation, merging, and deletion of multiple local branches that can be entirely independent of each other.

**Installation**
Visit [https://git-scm.com/downloads] and use the git installer and follow the steps, after you have  successfully installed, check for successful installation and version using thr following ccommand.

```python
git --version
```
**Set global configurations**
Now lets configure git by running the following global commands.

```python
git config --global user.name "user name"
git config --global user.email "email address"
```

**git init**
Initializes your local git repository as your master.

**git add . or git add "file name"**
To add all the files to staging area, run
```python
git add .
```
or add specific file using

```python
git add <file name>
```

**git commit -m "commit message"**
To save the changes to your repository with a message which describes the commit.

**git remote add origin "repository URL"**

When you have an online repository and would like to link it to your local repository, you can do so by running.

git remote add origin <repository URL>
          
**git push -u origin master**
          
To push the local repository to the online repository.

**git remote rename origin upstream**
Running this command will rename the online repository. Then add the new URL using "git remote add origin <repository URL>" and push the local to the online using "git push -u origin master"

**git clone <repository URL > **
          
To clone an online repository to your local machine.

**git revert**
Will reverse changes made by an earlier commit.

**git status**
To view the current status of the repository.

**git checkout**
View file from last commit and add it to staging area.

**git restore --staged**
Unstage files from last commit.

**git restore**
Restore file to original last commit.

**git log --online**
Show all commits.

**git log**
          
Display detail information about all commits.

git -b "branch name"
Running this command will create a new branch.

**git branch -a**
Show all branches.

**git checkout "branch name"**
          
Will move git from the master branch to the new branch.

**git merge "branch name"**
          
If there are new changes that needs to be added to the master, you can do so by switching back to the master branch.

**git branch -a**
          
To list branches.

**git pull**
          
To match the remote repository to the local.






