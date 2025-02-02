# Git and github:

## Git:
* On Local Machine; git repo tracks changes made  and saves versions(snapshots) of set of files/folders. 
* Repo is a folder or directory. to become a repository of git... git init(initialise)

* cd .. (goes to parent directory)
    - examples: /onedrive/Documents/github
        - cd .. 
        - /onedrive/Documents
* mkdir github : creates a folder 
* ls: lists all the files and folder
* Store github repos in a different place from where we store our credintials(keys).
* mkdire tech501-week1
* cd tech501-week1/ then git init; if made git add . before initialising the git repo this would give error(not a git repository). 
* git status: to check status 
* to rename branch to (main): 
```bash
git branch -M main
```
* there are 3 states of git: 
* 1- Modified/untracked(red):
- README.md

* 2-Staged(tracked, added to index)(green):
- git add .(. current dir)
- if any changes are made it will go back to modified (red). so git add . again


* 3- Committed(saved/snapshots): 
- git commit -m "added readme"
- If we do git status after commit we'll get tree clean.

 