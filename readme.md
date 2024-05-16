# Learn - Git

Welcome to the Git Command Reference! This guide offers a concise overview of the most common Git commands. Whether you're just starting out or in need of a quick refresher, these commands are fundamental to managing your repositories and optimizing your Git workflows.

This cheat sheet covers a broad range of commands from basic setup and configuration to advanced repository management. It is designed to be a valuable resource for both beginners and experienced Git users. For a deeper understanding of each command and their options, consult the Git documentation or use `git help [command]`.

## Setup and Config
1. **`git config --global user.name "[name]"`**: Set the name that will be attached to your commits and tags.
2. **`git config --global user.email "[email address]"`**: Set the email you will use for your commits.
3. **`git config --global core.editor "[editor]"`**: Set your preferred text editor.
4. **`git config --list`**: List all settings Git can find at different scopes.
5. **`git config user.name`**: View the name you have configured for git.
6. **`git config user.email`**: View the email you have configured for git.

## Creating Projects
7. **`git init`**: Initialize a local Git repository.
8. **`git clone [url]`**: Create a local copy of a remote repository.

## Basic Snapshotting
9. **`git status`**: Check the status of your files in the working directory and staging area.
10. **`git add [file]`**: Add a file as it looks now to your next commit (stage).
11. **`git reset [file]`**: Unstage a file while retaining the changes in the working directory.
12. **`git diff`**: Diff of what is changed but not staged.
13. **`git diff --staged`**: Diff of what is staged but not yet committed.
14. **`git commit -m "[descriptive message]"`**: Commit your staged content as a new commit snapshot.
15. **`git rm [file]`**: Remove a file from your working directory and the index.

## Branching and Merging
16. **`git branch`**: List your branches. A * will appear next to the currently active branch.
17. **`git branch [branch-name]`**: Create a new branch at the current commit.
18. **`git checkout [branch-name]`**: Switch to another branch and check it out into your working directory.
19. **`git merge [branch]`**: Merge the specified branch’s history into the current one.
20. **`git branch -d [branch-name]`**: Delete a branch.

## Sharing and Updating Projects
21. **`git push [alias] [branch]`**: Transmit local branch commits to the remote repository branch.
22. **`git pull`**: Fetch and merge any commits from the tracking remote branch.
23. **`git remote add [alias] [url]`**: Add a git URL as an alias.
24. **`git fetch [alias]`**: Fetch all branches from the given remote.

## Inspection and Comparison
25. **`git log`**: Show the commit history for the currently active branch.
26. **`git log --follow [file]`**: Show the commits that changed file, even across renames.
27. **`git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short`**: Best way to see the history.
28. **`git diff [first-branch]...[second-branch]`**: Show content differences between two branches.
29. **`git show [commit]`**: Show the metadata and content changes of the specified commit.

## Stashing and Cleaning
30. **`git stash`**: Stash your modifications to a dirty working directory.
31. **`git stash pop`**: Apply stashed changes back to your working directory.
32. **`git stash list`**: List stack-order of stashed file changes.
33. **`git stash drop`**: Discard the changes from the top of the stash stack.

## Tagging
34. **`git tag [commitID]`**: Tag a specific commit with a simple, memorable name.
35. **`git tag v1`**: Tag the current version of your project as v1.
36. **`git tag -d v1`**: Remove the tag.
37. **`git checkout v1`**: Checkout to the version tagged as v1.

## Git Rebase
38. **`git rebase [branch]`**: Apply any commits of current branch ahead of specified one.

## Setting up Aliases for Commands
39. **`git config --global alias.co checkout`**
40. **`git config --global alias.st status`**

## Undoing Changes
41. **`git revert [commit]`**: Generate a new commit that undoes all of the changes introduced in [commit], then apply it to the current branch.
42. **`git reset --hard [commit]`**: Reset your index and working directory to the state of a specific commit and discard all changes since then.
43. **`git reset --soft [commit]`**: Move the HEAD to a previous commit, keeping the staged changes.