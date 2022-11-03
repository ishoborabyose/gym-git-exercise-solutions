# GIT Exercise

## Bundle 1

### Exercise 1

```bash PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym
$ mkdir git-exercise

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym
$ cd git-exercise

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise
$ git init
Initialized empty Git repository in C:/Users/PC/Desktop/gym/git-exercise/.git/

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano README.md

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the nex
t time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git commit -m 'Initial commit'
[main (root-commit) a48a812] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote add origin https://github.com/ishoborabyose/git-exercise.git
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote -v
origin  https://github.com/ishoborabyose/git-exercise.git (fetch)
origin  https://github.com/ishoborabyose/git-exercise.git (push)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ ^C

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 232 bytes | 232.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git branch dev

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git branch
  dev
* main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout dev
Switched to branch 'dev'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git branch test

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git branch
* dev
  main
  test

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git checkout test
Switched to branch 'test'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (test)
$ git checkout dev
Switched to branch 'dev'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git branch
* dev
  main
  test

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git branch -d test
Deleted branch test (was a48a812).

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$
```

### Exercise 2

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ touch home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ ls
README.md  home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ nano home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ ls
README.md  home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git add .
warning: in the working copy of 'home.html', LF will be replaced by CRLF the nex
t time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ nano about.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git add .
warning: in the working copy of 'about.html', LF will be replaced by CRLF the ne
xt time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ nano team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash list
stash@{0}: WIP on dev: a48a812 Initial commit
stash@{1}: WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash
No local changes to save

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ ls
README.md  team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git add .
warning: in the working copy of 'team.html', LF will be replaced by CRLF the nex
t time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash list
stash@{0}: WIP on dev: a48a812 Initial commit
stash@{1}: WIP on dev: a48a812 Initial commit
stash@{2}: WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (f3c3f449f74e0ff8aa8eb47960604a1fd9ae6bcc)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash list
stash@{0}: WIP on dev: a48a812 Initial commit
stash@{1}: WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (14bfdfc5ff85d414228a6a68584bbd3d25c7b21f)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git add .

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git commit -m 'Set up the home and about page'
[dev bac1052] Set up the home and about page
 2 files changed, 20 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$  git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 530 bytes | 530.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/dev
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash list
stash@{0}: WIP on dev: a48a812 Initial commit

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash pop stash@{1}
fatal: log for 'stash' only has 1 entries

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (4aa65efa03bacc8bf9004194d2d3877d17c31fb8)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git reset --hard
HEAD is now at bac1052 Set up the home and about page

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$
```

## Bundle 2

### Exercise 1

```bash PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ ls
README.md  about.html  home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (dev)
$ git checkout -b ft-bundle2
Switched to a new branch 'ft-bundle2'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git status
On branch ft-bundle2
nothing to commit, working tree clean

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ nano service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git status
On branch ft-bundle2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git add .
warning: in the working copy of 'service.html', LF will be replaced by CRLF the
next time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git commit -m 'Create a service page'
[ft-bundle2 921e0d9] Create a service page
 1 file changed, 10 insertions(+)
 create mode 100644 service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git push
fatal: The current branch ft-bundle2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft-bundle2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git push --set-upstream origin ft-bundle2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 461 bytes | 461.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft-bundle2' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft-bundle2
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft-bundle2 -> ft-bundle2
branch 'ft-bundle2' set up to track 'origin/ft-bundle2'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$
```

### Exercise 2

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym
$ cd git-exercise

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ ls
README.md  about.html  home.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft-bundle2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 637 bytes | 91.00 KiB/s, done.
From https://github.com/ishoborabyose/git-exercise
   a48a812..219960b  main       -> origin/main
Updating a48a812..219960b
Fast-forward
 about.html   | 10 ++++++++++
 home.html    | 10 ++++++++++
 service.html | 10 ++++++++++
 3 files changed, 30 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git branch ft/service-redesign

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ nano service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git add .

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git commit -m 'Change some stuff'
[ft/service-redesign 255e73c] Change some stuff
 1 file changed, 3 insertions(+), 1 deletion(-)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 333 bytes | 333.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft/service-r
edesign
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ ls
README.md  about.html  home.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git add .

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git commit -m 'Added changes to services'
[main 0c11efb] Added changes to services
 1 file changed, 3 insertions(+), 1 deletion(-)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 342 bytes | 342.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishoborabyose/git-exercise.git
   219960b..0c11efb  main -> main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git branch
  dev
  ft-bundle2
  ft/service-redesign
* main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index d545516..a1d4c09 100644
--- a/service.html
+++ b/service.html
@@ -7,6 +7,6 @@
     <title>Service</title>
   </head>
Merge branch 'main' into ft/service-redesign

[ft/service-redesign ee7edee] Merge branch 'main' into ft/service-redesign

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git log
commit ee7edee06fecf6514f1d169f4e8813ed65cae842 (HEAD -> ft/service-redesign)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:40:08 2022 +0200

    Merge branch 'main' into ft/service-redesign

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main, main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5 (origin/ft/service-redesign)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Thu Nov 3 11:00:26 2022 +0200

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git status
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 370 bytes | 370.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishoborabyose/git-exercise.git
   255e73c..ee7edee  ft/service-redesign -> ft/service-redesign

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/service-redesign)
$
```
