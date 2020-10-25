# Day 2



## 6. Git works with changes not files
**Version control system that works with files:** you add file to source control and system tracks changes from that moment on.

**Version control system that works with changes:** notes current state of file.




## 7. Git's project history
`git log`
```
commit fc77b8d573c131eb5c4b2dfd3a2b6047e2695333 (HEAD -> main)
Author: Tanisha Bisht <agamyatani@gmail.com>
Date:   Sun Oct 25 14:48:10 2020 +0530
    remove some text

commit d0d7fa6929229eaaf841e00d8c680dd9372b6773
Author: Tanisha Bisht <agamyatani@gmail.com>
Date:   Sun Oct 25 14:44:35 2020 +0530
    initail commit
```

`git log --pretty=oneline`
```
fc77b8d573c131eb5c4b2dfd3a2b6047e2695333 (HEAD -> main) remove some text
d0d7fa6929229eaaf841e00d8c680dd9372b6773 initail commit
```

**The perfect log format:**<br/>
`git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short`
- `%h` hash of commit
- `%ad` commit date
- `%s` comment
- `%d` branch heads or tags
- `%an` name of the author
- `--graph` display git commit tree in ASCII graph layout
- `--date=short` keeps date format short and nice
```
* fc77b8d 2020-10-25 | remove some text (HEAD -> main) [Tanisha Bisht]
* d0d7fa6 2020-10-25 | initail commit [Tanisha Bisht]
```
- `--author=Tanisha` to see changes made only by Tanisha
- `--max-cout=2` to display recent 2 commits only
- `--since='5 minutes ago'` to diplay commits since 5 min




## 8. Set up aliases for git commands
```
git config --global alias.co checkout
git config --global alias.hist "log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short"
git config --global alias.st status
```

Alias for your command line (if it supports alias)
```
alias gs='git status '
alias ga='git add '
```




## 9. Getting older versions from commit history
- `git checkout <hash>` to go to the previous snapshots of the working directory. for <hash> first 7 characters are enough.
- `git checkout main` returns to the latest version in the master branch




## 10. Tag commits for future references
- `git tag v1` the current version of our project is referred as v1
- `git tag -d v1` to remove the tag
- `git checkout v1^` means checkout to the parent of v1
- `git checkout v1~1` means checkout to the first version prior to v1
- `HEAD` shows the commit you checked out
- `git tag` viewing all tags of the working directory




## 11. Discard changes made in working directory
`git checkout <file>`: When you want to discard the changes you made and return back to the version of last commit




## 12. Discard changes made in Staging area (before commiting)
`git reset HEAD <file>`: When you want to discard the changes you made and return back to the version of last commit




## 13. Cancelling commits
Make a commit with new changes that discard previous changes:
`git revert <hash>`

Remove last commits from the history of the repository:
1. give some tag name to the commit you want to remove (e.g. oops)
2. `git reset --hard <tag/hash to the previous commit u want to point to>`
REMEMBER: all commits afterwards will be deleted from the history of repository
3. `git log --online --all`
This returns the so called deleted commits too. This is because they are not listed in the master branch anymore but still remain in the repository. Now if we remove 
4. `git tag -d oops`
Oops tag has performed it’s function. Let us remove that tag and permit the garbage collector to delete referenced commit.




## 14. Changing commits
`git commit --amend -m "Add an author/email comment"` to change the recent commit.