## 👩🏻‍💻 THE GIT & GITHUB BOOTCAMP

- Version Control -> is software that tracks and manages changes to file over time.

### commands
- git --version -> to know the version
- |> to configure the name that Git will associate with your work
- git config --global user.name "James Gunn" 
- git config user.name // James Gunn
- |> Git email address to match your Github account
- git config --global user.email jamesgun@gmail.com
- git config user.email // jamesgun@gmail.com

### Git command
- ⚠️ Before running git init, use git status to verify that you are not currently inside a repo
- git status -> give information
- git init -> to cretate a new git repository.
- ls -a -> to show hidden files
- |WORKIKG DIRECTORY| git add |>STANGING AREA| git commit |>REPOSITORY|
- git add
- git add . -> to stage all changes at once (./)
- git add file1 file2
- git commit -m "my message"
- git commit -> open vim -> click ⌨️ a -> write commit ->  ⌨️ :wp
- git log -> to give information
    - git log --abbrev-commit
    - git log --oneline  *
- Amending Commits -> Suppose yoy just made a commit and then realized you forgot to include file! Or, you made a typo in the commit message that you want to correct. (just the previous commit)
    - git commit -m "some message"
    - git add forgotten_file
    - git commit --amend 
- .gitignore -> Ignoring Files 
    - 📋 Create a file called .gitignore in the root of a repository. Inside the file, we can grite patterns to tell Git wich files and folders to ignore (.DS_Store, folderName/, *.log(will ignore any files with the .log extension))

- ____________ workig with branches ____________
- HEAD -> master
    - HEAD is a pointer that refers to the current "location" in your repository. Ii points to a particular branch reference.
    - HEAD always points to the lastest commit you made on the master branch (or HEAD is the lastest commit on the branch I am)
- git branch -> to show branches of repo and to show what branch  I am
- git branch branch-name -> to make a new branch based upon the current HEAD
- git switch branch-name = git checkout branch-name
- git commit -a -m "This add and commit in one command" (👀 video 46)
- git checkout vs. git switch
    - git checkout branch-name
- git switch -c "branch-name" // create a new branch AND switch to it (-c -> create) (git checkout -b branch-name ?)
- (⚠️ 👀 v.48) When I have to switch branch without making a commit ->
    - git stash 
- ❌ Delete branch -> I can delete the branch when I am 
    - 1 -> git switch name-another-branch
    - 2 -> git branch -D name-delete-branch
- Rename a branch
    - 1 -> switch to branch we want to rename
        - git checkout branch-change-name
    - 2 -> git branch -m new-name

### ⚡️ Terminal crash course: navigation
- clear || command Q
- ls  -> to list the contents of your current directory
- ls Code || ls Code/website
- open Code
- open .
- pwd -> Print Working Directory (print the path to the working directory, where you currently are)
- cd -> Change Directory, to change and move between folders.
- cd folder
- cd .. -> to "back up" one directory

- 📄 Touch -> to create a FILE (or multiple) 
- touch app.js  (touch red.js orange.css yellow.js)
- git status

- 📁 mkdir (make directory) -> will create a new directtory ( or directories) 
- mkdir Code   || mkdir Code Illustration

- ❌ 📄 Deleting Files -> rm will delete a file or files (permanently)
- rm red.js  || rm red.js orange.css

- ❌ 📁 Deleting Folders -> rm -rf to delete directory (r=recursive, f=force)
- rm -rf Code  || rm -rf Code Illustration


### Mix _____________
- Atomic Commits -> When possible, a commit should encompass a single feature, change, or fix. Try to keep each commit focused on a single thing.

- git commit -> open vim -> click ⌨️ a -> write commit ->  ⌨️ :wp

- Installing gitKraken -> wwww.gitkraken.com