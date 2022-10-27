# git-faq

### List of common git commands with description:

| Command | Description |
| --- | --- |
| `git init` | git repo initialization |
| `git status` | show the working tree changes |
| `git add .` | add changes to staged |
| `git commit -m “...”` | commit changes with message |
| `git commit -a -m “...”` | same as `git add .` + `git commit -m "..."` (but only changes, no new files) |
| `git commit —amend -m “...”` | add staged changes to the last commit and change message |
| `git push` | update remote repo using local repo |
| `git push —delete origin [branch name]` | removing a branch from the repository |
| `git remote add origin [link]` | link a local repository to a remote one |
| `git remote -v` | shows URLs of remote repositories when listing your current remote connections |
| `git remote show origin` | info about branches in the project |
| `git fetch` | update local branches according to the remote ones (only download updates, not merge) |
| `git merge [branch name]` | merge the specified branch with the current branch. **Fast-forward** - when the branch into which we are merging hasn't been changed since the "spin-off". **Merge** - when a branch has changed and you want to update the local branch before push (pull, then a merge commit will appear). `git status` -> manual edit -> after merge conflict and manual editing -> `git add .` -> `git commit` (merge commit creation). ***Exit from the vi editor `:wq` : )***|
| `git pull` | same as `git fetch` + `git merge origin/main` (download new commits from a remote repository) |
| `git pull origin [commit id]` | download a specific branch from a remote repository |
| `git log` | commits history |
| `git diff` | difference between unstaged and the last commit |
| `git diff -staged` | difference between staged and the last commit |
| `git diff [commit id]` | the difference between a master and a specific commit |
| `git reset [commit id/head]` | rollback to a specific commit |
| `git checkout --` | switching between file versions/commits/branches |
| `git clean -n` | shows which unstaged changes will be deleted |
| `git clean -f` | delete unstaged changes |
| `git branch` | list of local branches and which branch we are in |
| `git branch -r` | list of remote branches |
| `git branch [name]` | create new branch with name |
| `git branch -d [branch name]` | delete local branch |
| `git rebase [branch name]` | move a branch before a specific commit to avoid merge commit |
| `git rebase --continue` | continue rebase after conflicts are resolved |
| `git rebase --skip` | skip commit that causes a merge conflict |
| `git rebase --abort` | abort the rebase operation and reset head to the original branch. If branch was provided when the rebase operation was started, then head will be reset to branch. Otherwise head will be reset to where it was when the rebase operation was started |
| `git rebase -i [head~3]` | interactive rebase (change the last 3 commits). During interactive rebase, `-i` enter input mode in the vi editor (ESC to exit input mode). After making changes -> `git add .` -> `git commit --amend` -> `git rebase --continue` |
| `git cherry-pick` | move a particular commit from one branch to another; `--edit` change the commit message; `--no-commit` transfer only changes from commit to staged; `-x` indicates in the message the hash of the commit from which the changes were taken; `--signoff` indicates in the commit message the user who made the cherry-pick |