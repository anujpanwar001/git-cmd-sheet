
# Git Basic Command Sheet
 
## Files basic

#### Create new Folder
- mkdir anuj

#### Create new file
- > index.html
- echo " " > index.html
- touch index.html

#### Check the Directory Files 
- ls

#### Check directory hidden files also likeit
- ls -a

#### Remove files or Folder
- rm -rf hello.text => for file
- rm -rf anuj => for folder

#### Insert data into file
- vi hello.text
   
   Save and exit from vi editor

    - hit esc key
    - :wq 

                       **or**

- nano hello.text       
    
    Save and exit from nano editor

     - ctrl+S
     - ctrl + X

#### Check file's data
- cat hello.text

## Git Basic

#### Initialize repo
- git init

#### Check how much changes I made
- git status

Those ***files are currently on our local device*** not into github or github history

#### Add all the files we made changes to
- git add .

  Add all files even if they are deleted too.

>                         or

- git add -A

  show all changes and add
          
>                 	  or

- git add hello.text

 We can add individual files by their names.


#### Add message to tell other people which changes I made
- git commit -m "Added hello.text file"

#### Add origin to our folder or Basically url to where our all code will store in online
- git remote add origin `Your repository link`

**example of repo link**

![images](/assister/repo-example.png)

#### check the currently added remote url or repository url
- git remote -v

#### Push those changes to online which we made it.
- git push origin main

#### If I add accidently any file and then we want to remove from stages area
- git restore --staged hello.text

#### How do i check all previous commits
- git log

#### If I want to remove the commit from log history then copy the hash code of the next one commit 
- git reset `hash code`

## Stash area

#### If I don't want to commit and also don't loose those files then add into stash area  
- git stash

#### Bring back all stashed files
- git stash pop

#### Delete file from stash area
- git stash clear


## Git Branch

#### Show current branch
- git branch --show-current

#### Check all branches
- git branch

#### Create new branch
- git checkout -b `branch name`

#### Switch between branches
- git checkout main

>                        or

- git switch main

### Why we create branches?
let's understand with one example

- In real world scenerio user use one main branch and if you pull direct code into main branch and suppose that code contains some bugs then users also face that issue that not good at all. So this is reason we create new branches.
- One branch has one pull request so that is second reson why we create new branch.
- It is recommanded if you work on new feature or might be fixing new bugs make sure you create new branch .
- If you pull data into one branch that might be cumbersome to read that code again.


## Contribute to other projects
- You don't have to access directly to make changes into other repo that might be terrified
- So First we fork that repo

![fork image](/assister/fork.png)

#### Clone your repo link not the upstream link
- git clone `your repo link`

![image](/assister/clone.png)

#### Add upstream url
- git remote add upstream `url`
 
 ![image](/assister/upstream.png)

#### You can't directly push changes to upstream url so you push changes in your repo and make pull request from that

#### Some times we changed some branch code like delete some files and that branch also merge to upstream url to push your changes
- git push orign -force

#### When our branch merged to upstream then github code can't be updated automatically and it also not possible to upstream make changes into our code, to update that changes in our repo well we write some cmd
- git fetch --all --prune 

   it fetch all files and also fetch deleted files as well

- git reset --hard upstream/main
   
   reset of my main branch origin to main branch of upstream and more simple words it will imitate upstream main branch and paste into my main branch


>                                     or

- git pull upstream main 

   internally it follow the same steps

