
KIIT@BT-2106319 MINGW64 ~/Desktop/git
$ git init
Initialized empty Git repository in C:/Users/KIIT/Desktop/git/.git/

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git config user.name
Sarthak

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ touch a.txt b.txt c.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git add .

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git commit -m "a b c are added"
[master (root-commit) 3ac294a] a b c are added
 3 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
 create mode 100644 b.txt
 create mode 100644 c.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git remote add origin https://github.com/SarthakAgarwal28/gittest.git

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git push origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 225 bytes | 225.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/SarthakAgarwal28/gittest.git
 * [new branch]      master -> master

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git branch car

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git branch bike

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git switch bike
Switched to branch 'bike'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ nano a.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ nano b.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git add .
warning: in the working copy of 'a.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'b.txt', LF will be replaced by CRLF the next time Git touches it

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git commit -m "edit a b"
[bike 6851858] edit a b
 2 files changed, 2 insertions(+)

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git switch
fatal: missing branch or commit argument

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git switch car
Switched to branch 'car'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ nano b.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ nano c.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git add .
warning: in the working copy of 'b.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'c.txt', LF will be replaced by CRLF the next time Git touches it

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git commit -m "b c edited"
[car 5387bc2] b c edited
 2 files changed, 3 insertions(+)

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git switch car
Already on 'car'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git switch bike
Switched to branch 'bike'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git merge car
Auto-merging b.txt
CONFLICT (content): Merge conflict in b.txt
Automatic merge failed; fix conflicts and then commit the result.

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike|MERGING)
$ git merge bike
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike|MERGING)
$ nano b.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike|MERGING)
$ git add b.txt

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike|MERGING)
$ git commit -m "resolved b"
[bike 24eca41] resolved b

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git switch car
Switched to branch 'car'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git merge car
Already up to date.

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git merge bike
Updating 5387bc2..24eca41
Fast-forward
 a.txt | 1 +
 b.txt | 4 ++++
 2 files changed, 5 insertions(+)

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git log
commit 24eca41c309e41ea4602d39ad0a8a25c56a9e436 (HEAD -> car, bike)
Merge: 6851858 5387bc2
Author: Sarthak <sarthak.agarwal2802@gmail.com>
Date:   Sat Apr 26 16:30:58 2025 +0530

    resolved b

commit 5387bc2a2086227d6e4b52cc9a813da9004c3eba
Author: Sarthak <sarthak.agarwal2802@gmail.com>
Date:   Sat Apr 26 16:29:43 2025 +0530

    b c edited

commit 6851858d2fceac1c3d8f406cb9663c1f803e1d30
Author: Sarthak <sarthak.agarwal2802@gmail.com>
Date:   Sat Apr 26 16:28:36 2025 +0530

    edit a b

commit 3ac294a10044081b5814308e8da3ce09cab0cc58 (origin/master, master)
Author: Sarthak <sarthak.agarwal2802@gmail.com>
Date:   Sat Apr 26 16:26:43 2025 +0530

    a b c are added

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git add .

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git commit -m  "merged car to bike"
On branch car
nothing to commit, working tree clean

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git switch car
Already on 'car'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git push origin car
Enumerating objects: 15, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (11/11), 839 bytes | 279.00 KiB/s, done.
Total 11 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'car' on GitHub by visiting:
remote:      https://github.com/SarthakAgarwal28/gittest/pull/new/car
remote:
To https://github.com/SarthakAgarwal28/gittest.git
 * [new branch]      car -> car

KIIT@BT-2106319 MINGW64 ~/Desktop/git (car)
$ git switch bike
Switched to branch 'bike'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git push origin bike
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'bike' on GitHub by visiting:
remote:      https://github.com/SarthakAgarwal28/gittest/pull/new/bike
remote:
To https://github.com/SarthakAgarwal28/gittest.git
 * [new branch]      bike -> bike

KIIT@BT-2106319 MINGW64 ~/Desktop/git (bike)
$ git switch master
Switched to branch 'master'

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git merge car
Updating 3ac294a..24eca41
Fast-forward
 a.txt | 1 +
 b.txt | 6 ++++++
 c.txt | 1 +
 3 files changed, 8 insertions(+)

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$ git push origin master
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/SarthakAgarwal28/gittest.git
   3ac294a..24eca41  master -> master

KIIT@BT-2106319 MINGW64 ~/Desktop/git (master)
$
