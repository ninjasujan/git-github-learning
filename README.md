# git-github-learning

**Git tracking and deleting files and directories.**

---

1. Deleting files in working directory.
   `git rm initial.txt`

---

2. Undoing `unstaged` changes.

   - using checkout
     `git checkout .
   - using restore -
     `git restore .` or `git restore initial.txt`

   - using checkout
     `git checkout .`
   - using restore -
     `git restore .` or `git restore initial.txt`

---

3. Deleting untracked files and directory.
   `git clean -dn`

---

4. Undoing staged changes
   Using both restore and checkout command.
   First need to unstage the chnages.
   `git restore --staged .`
   Second remove the unstaged changes.
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

---

#### Git advance command

1. Git stash
   Git stash command temporarily undo the untracked changes from WD.
   command: `git stash` - will go the initial
   `git stash push -m <message>`
   commit stage.

   Apply the stash
   To apply the stash we need to clean the untracked changes.(should have that initial commit)
   command: `git stash apply <stash_stage>`

   poping the git stash.
   remove the stash from list and add to the WD
   `git stash pop 0`

   Droping the stash
   `git stash drop <index>`

   ***

2. Git Reflog
   Reflog helps to bring the lost data back
   `git reflog`
   Gives all command history

---

3. Abort the merge
   `git merge --abort`
