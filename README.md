# git-faq

## List of common git commands with description:

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
| `git merge [branch name]` | merge the specified branch with the current branch. **fast-forward** - when the branch into which we are merging hasn't been changed since the "spin-off". **merge** - when a branch has changed and you want to update the local branch before push (pull, then a merge commit will appear). `git status` > manual edit > after merge conflict and manual editing > `git add .` > `git commit` (merge commit creation). ***exit from the vi editor - `:wq` ; )***|
| `git pull` | same as `git fetch` + `git merge origin/main` (download new commits from a remote repository) |
| `git pull origin [commit id]` | download a specific branch from a remote repository |
| `git log` | commits history |
| `git diff` | difference between unstaged and the last commit |
| `` | - |
| `` | - |
| `` | - |