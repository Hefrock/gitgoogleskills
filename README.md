# 💡: Curated Git quick references

## 📌 Push local code to GitHub
```
git init                                                            # Initializes new Git repo
git add .                                                           # Stages all new files in working directory
git commit -m "Initial commit: AI-powered decision support app"     # Snapshots staged files with a commit comment
git branch -M main                                                  # Renames current branch as main
git remote add origin https://github.com/Hefrock/the-tiebreaker.git # Links local to remote repo with "origin" nickname
git push -u origin main                                             # Upload local data to remote repo
```

## 🔀: Rebase Sync Routine
- This is helpful when collaborating when changes were made on the remote main repo. If our local version is behind main, we can catch up. 
```
git fetch origin                  # Downloads the latest branches and history from remote
git checkout main                 # Switches to the target branch
git pull origin main              # Pulls the latest updates to your local main
git checkout feature/new-feature  # Returns to your working branch
git rebase main                   # Integrates remote changes onto your branch
```

## ❄️ Pull remote repo and build into local working directory
- This is a useful routine for iterative local build testing
```
cd ~/dotfiles                                          # Change to working directory
git pull origin claude/testing-branch                  # Pull remote branch into local working directory
sudo nixos-rebuild switch --flake ~/dotfiles#laptop    # Nix code to build & switch
```

## 🧪 Test out remote repo before building
- Can test in realtime without creating another NixOS generation. Does not persist on reboot!
``` 
cd ~/dotfiles                                          # Change directory to working dir
git fetch origin                                       # Touch remote repo branches
git checkout claude/disable-trackpoint                 # Checkout the branch you want test locally
sudo nixos-rebuild test --flake .#laptop               # Test before building. Less NixOS generations
hyprctl reload                                         # Reload Hyprland ctrls 
```
