# Curated Git quick references

## Push local code to GitHub
```
git init                                                            # Initializes new Git repo
git add .                                                           # Stages all new files in working directory
git commit -m "Initial commit: AI-powered decision support app"     # Snapshots staged files with a commit comment
git branch -M main                                                  # Renames current branch as main
git remote add origin https://github.com/Hefrock/the-tiebreaker.git # Links local to remote repo with "origin" nickname
git push -u origin main                                             # Upload local data to remote repo
```

## Rebase Sync Routine
```
git fetch origin                  # Downloads the latest branches and history from remote
git checkout main                 # Switches to the target branch
git pull origin main              # Pulls the latest updates to your local main
git checkout feature/new-feature  # Returns to your working branch
git rebase main                   # Integrates remote changes onto your branch
```
