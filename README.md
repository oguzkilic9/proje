Bütün git komutları:

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop
$ cd proje

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje
$ git init
Initialized empty Git repository in C:/Users/kilic/Desktop/proje/.git/

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ touch yazilar.txt

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ touch yazi.txt

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git add .

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   yazi.txt
        new file:   yazilar.txt


kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git log
fatal: your current branch 'master' does not have any commits yet

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git commit -m "ilk commit"
[master (root-commit) 2c68c1f] ilk commit
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 yazi.txt
 create mode 100644 yazilar.txt

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git log
commit 2c68c1f900980a2526b076e198b4e719bbc87283 (HEAD -> master)
Author: oguz <kilicoguz9@gmail.com>
Date:   Sun Feb 2 12:19:22 2025 +0300

    ilk commit

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git remote add origin https://github.com/oguzkilic9/proje.git

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git push -u origin master
To https://github.com/oguzkilic9/proje.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/oguzkilic9/proje.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/oguzkilic9/proje.git'

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git pull origin master
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 845 bytes | 140.00 KiB/s, done.
From https://github.com/oguzkilic9/proje
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
fatal: refusing to merge unrelated histories

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git push -u origin master
To https://github.com/oguzkilic9/proje.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/oguzkilic9/proje.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ ^C

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ ^C

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git push -f origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 214 bytes | 214.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/oguzkilic9/proje.git
 + 6d1f94b...2c68c1f master -> master (forced update)

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git branch
* master

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git branch testing

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git branch
* master
  testing

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git chechkout testing
git: 'chechkout' is not a git command. See 'git --help'.

The most similar command is
        checkout

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (master)
$ git checkout testing
Switched to branch 'testing'

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git status
On branch testing
nothing to commit, working tree clean

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ touch test.txt

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git add .

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git commit -m "testing branch commit"
[testing 1d28b79] testing branch commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git push -u origin testing
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 249 bytes | 249.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'testing' on GitHub by visiting:
remote:      https://github.com/oguzkilic9/proje/pull/new/testing
remote:
To https://github.com/oguzkilic9/proje.git
 * [new branch]      testing -> testing
branch 'testing' set up to track 'origin/testing'.

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git stash
No local changes to save

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git touch deneme.txt
git: 'touch' is not a git command. See 'git --help'.

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git stash
No local changes to save

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ touch deneme.ttx


kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$
g
kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ rm deneme.ttx

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ rm deneme.txt
rm: cannot remove 'deneme.txt': No such file or directory

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ touch deneme.txt

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git stash
No local changes to save

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git add .

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$ git stash
Saved working directory and index state WIP on testing: 1d28b79 testing branch commit

kilic@DESKTOP-2KJTESK MINGW64 ~/Desktop/proje (testing)
$
