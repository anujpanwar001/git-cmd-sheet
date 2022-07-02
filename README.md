
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
