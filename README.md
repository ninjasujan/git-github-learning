# git-github-learning


**important command**

1. Deleting files in working directory.
    `git rm initial.txt`
---

2. Undoing `unstaged` changes.
    - using checkout
        `git checkout .`
    - using restore - 
        `git restore .` or `git restore initial.txt`
---
3. Deleting untracked files and directory.
   `git clean -dn`
---
4. Undoing staged changes
    Using restore and checkout command
    `git restore --staged .`
    `git checkout .`
---
5. Deleting the commit.
    - reset command.
        `git reset HEAD~1`
    soft reset deletes the commit and keeps changes in unstaged state.
    - soft reset. 
        `git reset --soft HEAD~1`
    soft reset deletes the commit and keeps changes in staged state.
    - hard reset
        `git reset --hard HEAD~1`
    deletes the commit and removes the content form working directory as well
---

6. Deleting branch
    - delete the branch if merged.
        `git branch -d feature`
    - delete branch forcefully.
        `git branch -D feature`