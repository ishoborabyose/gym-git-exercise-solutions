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
