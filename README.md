### Git Rebase

#### Rebase from master to feature branch without uncommitted changes in the feature branch

- Changes are happening in feature branch
```cmd
// Create a stash for local changes
git stash save "$stash_name"

// Check whether there are file changes in the remote origin
git fetch origin

// Switch to master branch
git switch master

// Pull all the changes
git pull origin

// Switch back to feature branch
git switch feature
 
// Rebase to origin/main branch to get the changes
git rebase origin/main

// Resolve conflicts manually 
git add .

// Use git bash for below
git rebase --continue

// Get local changes from stash
git stash pop

// Commit uncommitted changes
git commit -m "$commit_msg"

// Push to remote
git push origin
git push --force-with-lease
```

#### Rebase from master to feature branch with committed changes in the feature branch

```cmd

```