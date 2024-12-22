# Git

1. Config
```Bash
git config user.name # Get the username
git config user.email # Get the email
git config --global user.name "Sunny Bharne" # Set username 
git config --global user.email "example@email" # Set github email
```

2. Git imp commands
```Bash
git init # Initialise the git repo
git status
git add file1 file2
git commit -m "commit message"
git push
git log --all
git rm --cached File.name # Remove unstaged files
git restore --staged File.name # Remove unstaged files
git checkout -b branchName # Create and move to a new branch
git merge BranchName # move to main and then merge the code from Branch
git remote add origin https:/github.git # add remote repo
git clone https https:/github.git
git pull # get changes from remote (Can have conflicts)
```
