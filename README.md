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
