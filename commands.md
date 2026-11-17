# Git

## config
```bash
git config

-local = repository level
-global = user level
-system = system level
```

## workflow
```bash
# initialize a repository
>git init

#get status of working directory
>git status

# status in one single line
>git status -s

#status
XX = first character (status of file WRT staging area), second character (status of file WRT working directory)
?? : file is not yet committed in the repo
A_ : file is present in the staging are and will be added to the repo when committed
_M : file is modified and is present in the working directory
M_ : file is modified and is present in staging area
UU : the file has got at least one conflict

#add_the changes to staging area
>git add .

#commit the changes
>git commit -m "initial commit"

#get the logs
>git log
#oneliner
>got log --oneline
#graph = render the commit graph
>git log --oneline --graph
# color = enable color while rendering the commit graph
>git log --oneline --graph --color

#get the diff of current and previous file
>git diff

# go to previous version of commit
>git checkout

#remove all the changes from staging area and move then to working area
>git reset

# all the changes (from working dir to staging area will be reomoved) cation!!
>git reset --hard

```

## git internals

```bash

-hooks
    - contains the scripts to be executed on different events
-config
    - file contains local repo configuration
    - the config is restricted only for the current repo
-description
    - description about the repo
-objects
    - stores encrypted metadata
    - types
        -commit: object file which commit info 
        -tree: object file which contains the mapping of blob object file with their respective file names
        -blob: object file which stores the content of the file
    
-info

-refs
-Head
    - file which has entry of current branch
-branches
```


```bash
#find the type of the object
# -t: type
>git cat-file -t <<object-id>>

#find the readable content of an object
# -p: Pretty print
>git cat-file -p <<object-id>>



```

## branch

- a branch is a pointer to a commit object


```bash
#get list of branches
git branch

#create a new branch
git branch branch_name
# create new branch and checkout immediately
git checkout -b branch_name

# switch to other branch
git checkout branch_name

# merge the chages form one branch to another
# first checkout the branch in which you want to merge another branch 
git chechout main
git merge branch_name

#delete a branch
git branch -d branch_name
```


```bash
#squash merge
- collect all commit object of second branch and turn then into a single object
- then the single object gets merged in the source branch
- this will help git to reduce the commit.

```

## stash

```bash
#git the list of changes parked in the stash area
git stash list
#move the changes from working directory to stash area
git stash save "comment"

#get the details of a stash entry
git stash show stash@{0}

#apply the changes from stash area to working directory
git stash apply stash@{1}

#delete the stash object
git stash drop stash@{1}


```
