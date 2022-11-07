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

## Bundle 3

### Exercise 1

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git branch
  dev
  ft-bundle2
  ft/service-redesign
* main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ nano team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git add .
warning: in the working copy of 'team.html', LF will be replaced by CRLF the nex
t time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git commit -m 'Add team.html'
[ft/team-page f6dd9b6] Add team.html
 1 file changed, 10 insertions(+)
 create mode 100644 team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git push --set-upstream origin ft/team-page
To https://github.com/ishoborabyose/git-exercise.git
 ! [rejected]        ft/team-page -> ft/team-page (non-fast-forward)
error: failed to push some refs to 'https://github.com/ishoborabyose/git-exercis
e.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git push --set-upstreamb -f origin ft/team-page
error: unknown option `set-upstreamb'
usage: git push [<options>] [<repository> [<refspec>...]]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --repo <repository>   repository
    --all                 push all refs
    --mirror              mirror all refs
    -d, --delete          delete refs
    --tags                push tags (can't be used with --all or --mirror)
    -n, --dry-run         dry run
    --porcelain           machine-readable output
    -f, --force           force updates
    --force-with-lease[=<refname>:<expect>]
                          require old value of ref to be at this value
    --force-if-includes   require remote updates to be integrated locally
    --recurse-submodules (check|on-demand|no)
                          control recursive pushing of submodules
    --thin                use thin pack
    --receive-pack <receive-pack>
                          receive pack program
    --exec <receive-pack>
                          receive pack program
    -u, --set-upstream    set upstream for git pull/status
    --progress            force progress reporting
    --prune               prune locally removed refs
    --no-verify           bypass pre-push hook
    --follow-tags         push missing but relevant tags
    --signed[=(yes|no|if-asked)]
                          GPG sign the push
    --atomic              request atomic transaction on remote side
    -o, --push-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git push --set-upstream -f origin ft/team-page
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 742 bytes | 742.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/ishoborabyose/git-exercise.git
 + b6f042f...f6dd9b6 ft/team-page -> ft/team-page (forced update)
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git branch
  dev
  ft-bundle2
* ft/contact-page
  ft/service-redesign
  ft/team-page
  main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git log
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
commit f6dd9b638121af22c79f04b1a817787f9a6894f3 (HEAD -> ft/team-page, origin/ft
/team-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:17:40 2022 +0200

    Add team.html

commit c1e84d2e4920d71c9d87718e984d2def1401d51e (main, ft/service-redesign, ft/c
ontact-page)
Merge: 255e73c 0c11efb
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Fri Nov 4 18:07:47 2022 +0200

    solved conflicts

commit 0c11efb6e998819743c5d6fe2c8d8a5f726df77c (origin/main)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:33:48 2022 +0200

    Added changes to services

commit 255e73c83bb04f16b0f807b87164d1d74819a0b5
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Thu Nov 3 21:27:58 2022 +0200

    Change some stuff

commit 219960b2b9be746c52d57c6179a98d2a6917b20b
Merge: a48a812 921e0d9
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Thu Nov 3 11:00:26 2022 +0200

    Merge pull request #1 from ishoborabyose/ft-bundle2

    Add a new HTML Pages to the project

commit 921e0d9dbda92a1c805efa6bb300354bb365fd86 (origin/ft-bundle2, ft-bundle2)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Date:   Wed Nov 2 08:19:31 2022 +0200

    Create a service page

commit bac1052427769761c3383ea62dcd4fbdcba16de8 (origin/dev, dev)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git branch
  dev
  ft-bundle2
  ft/contact-page
  ft/service-redesign
* ft/team-page
  main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git cherry-pick f6dd9b638121af22c79f04b1a817787f9a6894f3
[ft/contact-page 1aad0a9] Add team.html
 Date: Fri Nov 4 18:17:40 2022 +0200
 1 file changed, 10 insertions(+)
 create mode 100644 team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ ls
README.md  about.html  home.html  service.html  team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ nano contact.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git add .
warning: in the working copy of 'contact.html', LF will be replaced by CRLF the
next time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git commit -m 'add contact page'
[ft/contact-page c19d766] add contact page
 1 file changed, 10 insertions(+)
 create mode 100644 contact.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$
    git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 696 bytes | 696.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft/contact-p
age
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/contact-page)
$  git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$ nano faq.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$ git add .
warning: in the working copy of 'faq.html', LF will be replaced by CRLF the next
 time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$ git commit -m 'added faq page'
[ft/faq-page 131564b] added faq page
 1 file changed, 10 insertions(+)
 create mode 100644 faq.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$  git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$  git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 448 bytes | 448.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft/faq-page
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$ git log
commit 131564bb0de9c77df7226b6e54a67b2b138aacd0 (HEAD -> ft/faq-page, origin/ft/
faq-page)
Author: ishoborabyose <ishoborabyosebeatrice@gmail.com>
Revert "Add team.html"


[ft/faq-page 4cf5236] Revert "Add team.html"
 1 file changed, 10 deletions(-)
 delete mode 100644 team.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 275 bytes | 275.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ishoborabyose/git-exercise.git
   131564b..4cf5236  ft/faq-page -> ft/faq-page

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$
```

### Exercise 2

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$  git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ ls
README.md  about.html  home.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git add .

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git commit -m 'added changes to home'
[main bcac965] added changes to home
 1 file changed, 3 insertions(+), 1 deletion(-)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 323 bytes | 323.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishoborabyose/git-exercise.git
   0c11efb..bcac965  main -> main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ ls
README.md  about.html  contact.html  faq.html  home.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ nano home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git add .

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git commit -m 'modify home'
[ft/home-page-redesign bff66ab] modify home
 1 file changed, 1 insertion(+)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.50 KiB | 1.50 MiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft/home-page
-redesign
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$
```

## Bundle 4

### Exercise 1

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote add git-copy git@github.com/ishoborabyose/git-exercise-clone.git

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote
git-copy
origin

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ ls
README.md  about.html  home.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git commit -m 'add some changes on home'
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git add .

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git commit -m 'add some changes on home'
[main bec043d] add some changes on home
 1 file changed, 1 insertion(+)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 310 bytes | 310.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishoborabyose/git-exercise.git
   bcac965..bec043d  main -> main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push git-copy
fatal: 'git@github.com/ishoborabyose/git-exercise-clone.git' does not appear to
be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push git-copy main
fatal: 'git@github.com/ishoborabyose/git-exercise-clone.git' does not appear to
be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote --list
error: unknown option `list'
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--m
irror=<fetch|push>] <name> <url>
   or: git remote rename [--[no-]progress] <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)..
.]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote -v
git-copy        git@github.com/ishoborabyose/git-exercise-clone.git (fetch)
git-copy        git@github.com/ishoborabyose/git-exercise-clone.git (push)
origin  https://github.com/ishoborabyose/git-exercise.git (fetch)
origin  https://github.com/ishoborabyose/git-exercise.git (push)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push git-copy main
fatal: 'git@github.com/ishoborabyose/git-exercise-clone.git' does not appear to
be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote add git-copy https://github.com/ishoborabyose/git-exercise-clone.git
error: remote git-copy already exists.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git remote set-url git-copy https://github.com/ishoborabyose/git-exercise-clone.git

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push git-copy main
Enumerating objects: 26, done.
Counting objects: 100% (26/26), done.
Delta compression using up to 8 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (26/26), 2.83 KiB | 964.00 KiB/s, done.
Total 26 (delta 14), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (14/14), done.
To https://github.com/ishoborabyose/git-exercise-clone.git
 * [new branch]      main -> main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push origin
Everything up-to-date

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$
```

### Exercise 2

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ nano footer.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ git status
On branch ft/footer
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        footer.html

nothing added to commit but untracked files present (use "git add" to track)

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ git add .
warning: in the working copy of 'footer.html', LF will be replaced by CRLF the n
ext time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ git commit -m 'added footer feture'
[ft/footer 1a9a4f4] added footer feture
 1 file changed, 10 insertions(+)
 create mode 100644 footer.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ git push
fatal: The current branch ft/footer has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/footer

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ git push --set-upstream origin ft/footer
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 454 bytes | 454.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft/footer
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/footer)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$ git status
On branch ft/squashing
nothing to commit, working tree clean

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$ git merge --squash ft/footer
Updating bec043d..1a9a4f4
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 10 ++++++++++
 1 file changed, 10 insertions(+)
 create mode 100644 footer.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$ git commit -m 'footer changes squashing'
[ft/squashing 11f7bbe] footer changes squashing
 1 file changed, 10 insertions(+)
 create mode 100644 footer.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$ git push
fatal: The current branch ft/squashing has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/squashing

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$  git push --set-upstream origin ft/squashing
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 459 bytes | 459.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/ishoborabyose/git-exercise/pull/new/ft/squashin
remote:
To https://github.com/ishoborabyose/git-exercise.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$
```

## Bundle 5

### Exercise 1

```bash
PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (ft/squashing)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git pull
Already up to date.

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano index.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ ls
README.md  about.html  home.html  index.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano home.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ nano index.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ ls
README.md  about.html  home.html  index.html  service.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git add .
warning: in the working copy of 'index.html', LF will be replaced by CRLF the ne
xt time Git touches it

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   index.html


PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git add index
fatal: pathspec 'index' did not match any files

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push
Everything up-to-date

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git commit -m 'added index'
[main 1277749] added index
 1 file changed, 15 insertions(+)
 create mode 100644 index.html

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 475 bytes | 475.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ishoborabyose/git-exercise.git
   bec043d..1277749  main -> main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$ git push git-copy
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 475 bytes | 475.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ishoborabyose/git-exercise-clone.git
   bec043d..1277749  main -> main

PC@DESKTOP-4QE8GRN MINGW64 ~/Desktop/gym/git-exercise (main)
$
```
