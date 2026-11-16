# G

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
UU :




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

```

