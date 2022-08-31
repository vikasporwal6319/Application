git init============>>>>>>>Initialized empty Git repository in C:/Working/.git/
git config --global user.name "Vikas Porwal"
git config --global user.email "vikasporwal@live.com"
================================================================================
git add . ==========================>To add file to staging area
PS C:\Working> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   FileA
        new file:   FileB
====================================================================================
>>>>git commit -m "This is initial commit"
[main (root-commit) f4d3b4c] This is initial commit
 2 files changed, 2 insertions(+)
 create mode 100644 FileA
 create mode 100644 FileB
 =================================================================================
PS C:\Working> git status
On branch main
nothing to commit, working tree clean
PS C:\Working> 
===================================================================================
PS C:\Working> git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   FileB

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Working> git add FileB.txt
fatal: pathspec 'FileB.txt' did not match any files
PS C:\Working> git add FileB    
PS C:\Working> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   FileB

PS C:\Working> git commit -m "Changes made to FileB"
[main 05613e2] Changes made to FileB
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Working> git status
On branch main
nothing to commit, working tree clean
PS C:\Working> 
===================================================================================
PS C:\Working> git log
commit 05613e2c12ebc9007e79055845cd763dea84d18d (HEAD -> main)
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 01:33:34 2022 +0530

    Changes made to FileB

commit f4d3b4cd7387429c13f423a90e2fac33717200ea
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 00:51:57 2022 +0530

    This is initial commit
PS C:\Working> git checkout f4d3b4cd7387429c13f423a90e2fac33717200ea
Note: switching to 'f4d3b4cd7387429c13f423a90e2fac33717200ea'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at f4d3b4c This is initial commit
PS C:\Working> git log -all
error: switch `l' expects a numerical value
PS C:\Working> git log --all
commit 05613e2c12ebc9007e79055845cd763dea84d18d (main)
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 01:33:34 2022 +0530

    Changes made to FileB

commit f4d3b4cd7387429c13f423a90e2fac33717200ea (HEAD)
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 00:51:57 2022 +0530

    This is initial commit
PS C:\Working> git checkout 05613e2c12ebc9007e79055845cd763dea84d18d
Previous HEAD position was f4d3b4c This is initial commit
HEAD is now at 05613e2 Changes made to FileB
PS C:\Working> 
=======================================================================================
**********************Unstaging a file**********************
PS C:\Working> git status
HEAD detached at 05613e2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   FileB

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Working> git checkout main
Switched to branch 'main'
M       FileB
PS C:\Working> git checkout main
Already on 'main'
M       FileB
PS C:\Working> git status       
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   FileB

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Working> git rm --cached FileB 
rm 'FileB'
PS C:\Working> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    FileB

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        FileB

PS C:\Working> git add .
PS C:\Working> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   FileB

PS C:\Working> git log
commit 05613e2c12ebc9007e79055845cd763dea84d18d (HEAD -> main)
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 01:33:34 2022 +0530

    Changes made to FileB

commit f4d3b4cd7387429c13f423a90e2fac33717200ea
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 00:51:57 2022 +0530

    This is initial commit
PS C:\Working> git commit -m "Previous state"
[main 1f98dfd] Previous state
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Working> 
PS C:\Working>
PS C:\Working> git log --all
commit 1f98dfd3d600d9018f8c72dc99f5ba8434cfd83b (HEAD -> main)
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 11:50:14 2022 +0530

    Previous state

commit 05613e2c12ebc9007e79055845cd763dea84d18d
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 01:33:34 2022 +0530

    Changes made to FileB

commit f4d3b4cd7387429c13f423a90e2fac33717200ea
Author: Vikas Porwal <vikasporwal@live.com>
Date:   Wed Aug 31 00:51:57 2022 +0530

    This is initial commit
PS C:\Working> 