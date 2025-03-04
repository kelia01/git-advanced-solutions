<details>
  <summary>Part 1 - Exercise 1</summary>

  # Exercise 1
   <!--My terminal history was lost I only wrote the commands-->

  ```bash
  git clone https://github.com/kelia01/Git-advanced-exercises.git
touch test{1..4}.md\
git add test1.md && git commit -m "chore: Create initial file"\
git add test2.md && git commit -m "chore: Create another file"\
git add test3.md && git commit -m "chore: Create third and fourth files"
git status
git log
git add test4.md
git commit --amend -m "Add the fourth file to my commit"
git log --oneline
git statusgit clone https://github.com/kelia01/Git-advanced-exercises.git
touch test{1..4}.md\
git add test1.md && git commit -m "chore: Create initial file"\
git add test2.md && git commit -m "chore: Create another file"\
git add test3.md && git commit -m "chore: Create third and fourth files"
git status
git log
git add test4.md
git commit --amend -m "Add the fourth file to my commit"
git log --oneline
git statusgit clone https://github.com/kelia01/Git-advanced-exercises.git
touch test{1..4}.md\
git add test1.md && git commit -m "chore: Create initial file"\
git add test2.md && git commit -m "chore: Create another file"\
git add test3.md && git commit -m "chore: Create third and fourth files"
git status
git log
git add test4.md
git commit --amend -m "Add the fourth file to my commit"
git log --oneline
git status
```
</details>

<details>
  <summary>Part 1 - Exercise 2</summary>
  
  # Exercise 2
  ```bash
git rebase -i HEAD~2
git rebase --abort
git rebase -i HEAD~2
git commit --amend -m "Create second file"
[detached HEAD e16fcd2] Create second file
 Date: Wed Feb 26 14:58:56 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
gymimbyino@Imbyinos-iMac-2 Git-advanced-exercises % git rebase --continue
```

</details>

<details>
  <summary>Part 1 - Exercise 3</summary>
  
  # Exercise 3
  ```bash
     PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 
     
     `git rebase -i --root`
fatal: Could not resolve HEAD to a commit
From https://github.com/kelia01/Git-advanced-exercises
 * branch            main       -> FETCH_HEAD
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git reset --hard origin/main`
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git log --oneline`
e16fcd2 Create second file
e723746 chore: Create initial file
pick e16fcd2 Create second file
fatal: invalid upstream 'rebase'
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git rebase -i rebase HEAD~2`
fatal: invalid upstream 'rebase'
pick e723746 chore: Create initial file
#
>>
Successfully rebased and updated refs/heads/main.
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git rebase -i HEAD~3`
fatal: invalid upstream 'HEAD~3'
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git rebase -i --root`
>> 
[detached HEAD ca81bc1] chore: Create initial file
 Date: Wed Feb 26 14:58:56 2025 +0200
 create mode 100644 test1.md
 create mode 100644 test2.md
 Successfully rebased and updated refs/heads/main.
 PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 
 
 `git rebase --continue`
 PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 
 
 `git log --oneline`
 46bdcda (HEAD -> main) Add the fourth file to my commit
 ca81bc1 chore: Create initial file
  ```
  </details>

  <details>
  <summary>Part 1 - Exercise 4</summary>
  
  # Exercise 4

  ```bash
  PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 
  
  `git rebase -i HEAD~1`
>>
Stopped at 46bdcda...  Add the fourth file to my commit
You can amend the commit now, with
Once you are satisfied with your changes, run

  `git rebase --continue`
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git commit -m 'Add the third file'`
[detached HEAD 61204b7] Add the third file
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git add test4.md`
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git commit -m 'Add the fourth file'`
[detached HEAD 30dd1fd] Add the fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git status`
interactive rebase in progress; onto ca81bc1
Last command done (1 command done):
   edit 46bdcda Add the fourth file to my commit
You are currently editing a commit while rebasing branch 'main' on 'ca81bc1'.
  (use "git rebase --continue" once you are satisfied with your changes)

nothing to commit, working tree clean
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git rebase --continue`
Successfully rebased and updated refs/heads/main.
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git log --oneline`
30dd1fd (HEAD -> main) Add the fourth file
61204b7 Add the third file
ca81bc1 chore: Create initial file
  ```
  </details>

  <details>
  <summary>Part 1 - Exercise 5</summary>
  
  # Exercise 5

  ```bash
   `git rebase -i HEAD~1`
   `git rebase --continue `
   `git log --oneline `
  ```
   <!--My terminal history was lost I only wrote the commands-->
  </details>

  <details>
  <summary>Part 1 - Exercise 6</summary>
  
  # Exercise 6
   ```bash
     HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ touch unwanted.txt
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git add unwanted.txt`
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git commit -m 'Unwanted commit'`
[main cddd7e5] Unwanted commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 unwanted.txt
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git rebase -i`
warning: skipped previously applied commit 3177010
hint: Disable this message with "git config advice.skippedCherryPicks false"
interactive rebase in progress; onto f5ec4e4
Last command done (1 command done):
   pick ca81bc1 chore: Create initial file
Next command to do (1 remaining command):
   drop cddd7e5 Unwanted commit
  (use "git rebase --edit-todo" to view and edit)
You are currently rebasing branch 'main' on 'f5ec4e4'.
  (all conflicts fixed: run "git rebase --continue")

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git rebase --skip'
Could not apply ca81bc1... chore: Create initial file
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git rebase --continue`
Successfully rebased and updated refs/heads/main.
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git log --oneline`
f5ec4e4 (HEAD -> main, origin/main) Add the fourth file to my commit
e16fcd2 Create second file
e723746 chore: Create initial file
   ```
  </details>

   <details>
  <summary>Part 1 - Exercise 7</summary>
  
  # Exercise 7
  ```bash
  HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git log --oneline
3770c2f (HEAD -> main) Create second file
5c086f4 Add the fourth file to my commit
e723746 chore: Create initial file
  ```

  </details>

 <details>
  <summary>Part 1 - Exercise 8</summary>
  
  # Exercise 8
  ```bash
  HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/branch)

$ git log
commit 81b00608680bf15a6de11406a00b50f89ee54089 (HEAD -> ft/branch)
Author: Kelia Iradukunda <iradukundakelia@gmail.com>
Date:   Fri Feb 28 18:25:16 2025 +0200

    Implemented test 5

commit 3770c2f43e0d9d20885df9441afbe3c4118a87fd (main)
Author: kelia01 <iradukundakelia@gmail.com>
Date:   Wed Feb 26 14:58:56 2025 +0200

    Create second file

commit 5c086f4a4d30486720f7720ae51685c77ad0a980
Author: kelia01 <iradukundakelia@gmail.com>
Date:   Wed Feb 26 14:58:56 2025 +0200

    Add the fourth file to my commit

commit e7237469a2b2e33ebfb3649e9ced8e4aaf3554fe
Author: kelia01 <iradukundakelia@gmail.com>

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/branch)

$ git switch main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 2 and 2 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)
  HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 2 and 2 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   test5.md
        HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git commit -m 'Add a test 5 file'
[main 5886f76] Add a test 5 file
 1 file changed, 2 insertions(+)
 create mode 100644 test5.md

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git diff

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git show
commit 5886f76a59ca014ddd2f1c865b0dbc686bfd3e4a (HEAD -> main)
Author: Kelia Iradukunda <iradukundakelia@gmail.com>
Date:   Fri Feb 28 18:58:32 2025 +0200

    Add a test 5 file

diff --git a/test5.md b/test5.md
new file mode 100644
index 0000000..ce79ac4
--- /dev/null
+++ b/test5.md
@@ -0,0 +1,2 @@
+This is the file for testing 
+cherry-picking commits
\ No newline at end of file
  ```
  </details>

  <details>
  <summary>Part 1 - Exercise 9</summary>
  
  # Exercise 9

  ```bash
  HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git log --graph
* commit 5886f76a59ca014ddd2f1c865b0dbc686bfd3e4a (HEAD -> main)
| Author: Kelia Iradukunda <iradukundakelia@gmail.com>
| Date:   Fri Feb 28 18:58:32 2025 +0200
|
|     Add a test 5 file
|
* commit 3770c2f43e0d9d20885df9441afbe3c4118a87fd
| Author: kelia01 <iradukundakelia@gmail.com>
| Date:   Wed Feb 26 14:58:56 2025 +0200
|
|     Create second file
|
* commit 5c086f4a4d30486720f7720ae51685c77ad0a980
| Author: kelia01 <iradukundakelia@gmail.com>
| Date:   Wed Feb 26 14:58:56 2025 +0200
|
|     Add the fourth file to my commit
|
* commit e7237469a2b2e33ebfb3649e9ced8e4aaf3554fe
  Author: kelia01 <iradukundakelia@gmail.com>
  Date:   Wed Feb 26 14:58:56 2025 +0200

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git log --graph --oneline --all --decorate
* 5886f76 (HEAD -> main) Add a test 5 file
| * 81b0060 (ft/branch) Implemented test 5
|/
* 3770c2f Create second file
* 5c086f4 Add the fourth file to my commit
| * f5ec4e4 (origin/main) Add the fourth file to my commit
| * e16fcd2 Create second file
|/
* e723746 chore: Create initial file
  ```
  </details>

<details>
  <summary>Part 1 - Exercise 10</summary>
  
  # Exercise 10

 ```bash
  HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
  $ git reflog
5886f76 (HEAD -> main) HEAD@{0}: commit: Add a test 5 file     
3770c2f HEAD@{1}: checkout: moving from ft/branch to main      
81b0060 (ft/branch) HEAD@{2}: commit: Implemented test 5       
3770c2f HEAD@{3}: checkout: moving from main to ft/branch      
3770c2f HEAD@{4}: rebase (finish): returning to refs/heads/main
3770c2f HEAD@{5}: rebase (pick): Create second file
5c086f4 HEAD@{6}: rebase (pick): Add the fourth file to my commit
e723746 HEAD@{7}: rebase (start): checkout HEAD~2
f5ec4e4 (origin/main) HEAD@{8}: rebase (finish): returning to refs/heads/main     
f5ec4e4 (origin/main) HEAD@{9}: rebase (start): checkout refs/remotes/origin/main 
f5ec4e4 (origin/main) HEAD@{10}: rebase (finish): returning to refs/heads/main    
f5ec4e4 (origin/main) HEAD@{11}: rebase (start): checkout HEAD~2
f5ec4e4 (origin/main) HEAD@{12}: rebase (finish): returning to refs/heads/main    
f5ec4e4 (origin/main) HEAD@{13}: rebase (start): checkout HEAD~
f5ec4e4 (origin/main) HEAD@{14}: rebase (finish): returning to refs/heads/main    
f5ec4e4 (origin/main) HEAD@{15}: rebase (start): checkout refs/remotes/origin/main
f5ec4e4 (origin/main) HEAD@{16}: rebase (finish): returning to refs/heads/main    
f5ec4e4 (origin/main) HEAD@{17}: rebase (start): checkout refs/remotes/origin/main
f5ec4e4 (origin/main) HEAD@{18}: rebase (finish): returning to refs/heads/main    
f5ec4e4 (origin/main) HEAD@{19}: rebase (start): checkout refs/remotes/origin/main
cddd7e5 HEAD@{20}: commit: Unwanted commit
```
</details>

## Part two

<details>
  <summary>Part 2 - Exercise 1,2,3,4</summary>
  
  # Exercise 1,2,3,4

```bash
HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git checkout -b ft/new-feature
Switched to a new branch 'ft/new-feature'

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/new-feature)
$ touch feature.txt

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/new-feature)
$ git add feature.txt

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/new-feature)

$ git commit -m 'Implemented core functionality for new feature'
[ft/new-feature 071b028] Implemented core functionality for new feature
 1 file changed, 2 insertions(+)
 create mode 100644 feature.txt

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/new-feature)

$ git switch main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 3 and 2 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ touch readme.txt

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git add readme.txt

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git commit -m 'Updated project readme.'
[main 693125b] Updated project readme.
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt
 Merge branch 'main' of https://github.com/kelia01/Git-advanced-exercises

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 4 and 2 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

nothing to commit, working tree clean

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git pull
Merge made by the 'ort' strategy.

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)

$ git push
Enumerating objects: 12, done.
Counting objects: 100% (12/12), done.
Delta compression using up to 4 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (10/10), 1.13 KiB | 144.00 KiB/s, done.
Total 10 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
To https://github.com/kelia01/Git-advanced-exercises.git
   f5ec4e4..7cde4e9  main -> main

   HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/branch)
$ git push -u origin ft/branch
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 319 bytes | 106.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/branch' on GitHub by visiting:
remote:      https://github.com/kelia01/Git-advanced-exercises/pull/new/ft/branch
remote:
To https://github.com/kelia01/Git-advanced-exercises.git
 * [new branch]      ft/branch -> ft/branch
branch 'ft/branch' set up to track 'origin/ft/branch'.
 ```
 </details>

 <details>
  <summary>Part 2 - Exercise 5</summary>
  
  # Exercise 5

```bash
HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git merge ft/new-feature
Merge made by the 'ort' strategy.
 feature.txt | 2 ++
 1 file changed, 2 insertions(+)
 create mode 100644 feature.txt 

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git branch -d ft/new-feature
Deleted branch ft/new-feature (was 071b028).
```
</details>

<details>
  <summary>Part 2 - Exercise 6,7</summary>
  
  # Exercise 6,7
```bash
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git log --oneline`
7cde4e9 (origin/main) Merge branch 'main' of https://github.com/kelia01/Git-advanced-exercises
071b028 Implemented core functionality for new feature
5886f76 Add a test 5 file
3770c2f Create second file
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git checkout -b ft/new-branch-from-commit 5886f76`
Switched to a new branch 'ft/new-branch-from-commit'

## Exercise 7

Switched to branch 'ft/new-branch-from-commit'
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git add test5.md`
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git commit -m 'Add a sentence to merge efficiently on ex7'`
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> 

`git switch main`
Switched to branch 'main'
  (use "git push" to publish your local commits)
PS C:\Users\HP\OneDrive\Documents\Git-advanced-exercises> git merge ft/new-branch-from-commit 
Auto-merging test5.md
CONFLICT (content): Merge conflict in test5.md
Automatic merge failed; fix conflicts and then commit the result.
```
</details>
<details>
  <summary>Part 2 - Exercise 8</summary>
  
  # Exercise 8
```bash
HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (|REBASE)
$ rm -rf .git/rebase-merge

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git branch
  ft/branch
  ft/improved-branch-name
* main

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git checkout ft/improved-branch-name
Switched to branch 'ft/improved-branch-name'

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (ft/improved-branch-name)
$ git rebase main
Successfully rebased and updated refs/heads/ft/improved-branch-name.
```
</details>
<details>
  <summary>Part 2 - Exercise 9</summary>
  
  # Exercise 9
```bash
HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (|REBASE)
$ git branch -m ft/new-branch-from-commit ft/improved-branch-name

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (|REBASE)
$ git branch
  ft/branch
  ft/improved-branch-name
* main
```
</details>

<details>
  <summary>Part 2 - Exercise 10</summary>

  # Exercise 10
```bash
HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises (main)
$ git checkout 693125b
Note: switching to '693125b'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 693125b Updated project readme.

HP@DESKTOP-R0HLVRA MINGW64 ~/OneDrive/Documents/Git-advanced-exercises ((693125b...))
```
</details>