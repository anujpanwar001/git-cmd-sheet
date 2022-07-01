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

#### Remove files or Folder
- rm -rf hello.text => for file
- rm -rf anuj => for folder

## Git Basic

#### Initialize repo
- git init

#### Check how much changes I made
- git status

Those ***files are currently on our local device*** not into github or github history

#### Add all the files we made changes to
- git add .
> Add all files even if they are deleted too.

        **or**

- git add -A 
> Show all changes and add
          
	**or**

- git add hello.text
> We can add individual files by their names.


#### Add message to tell other people which changes I made
- git commit -m "Added hello.text file"

#### Add origin to our folder or Basically url to where our all code will store in online
- git remote add origin `Your repository link`

#### Push those changes to online which we made it.
- git push origin main

