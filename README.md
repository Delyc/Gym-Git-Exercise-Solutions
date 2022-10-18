# Gym-Git-Exercise-Solutions




BUNDLE 1

#EXERCISE 1

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop
$ cd Gym-Git-Exercise-Solutions/

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ touch index.txt

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ mv index.txt index.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ code .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git commit -m "created index.txt page and renamed it to index.html page"
[main 82e9f14] created index.txt page and renamed it to index.html page
 1 file changed, 12 insertions(+)
 create mode 100644 index.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 509 bytes | 509.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
   708dc8c..82e9f14  main -> main

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (test)
$ git checkout dev
Switched to branch 'dev'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git branch -d test
Deleted branch test (was 82e9f14).



#EXERCISE 2


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ touch home.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ touch about.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ touch team.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page
stash@{1}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page
stash@{2}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ ^C

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash apply stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page
stash@{1}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page
stash@{2}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ ^C

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash apply stash@{2}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git commit -m "popped home and about stashes"
[dev d6c80f0] popped home and about stashes
 3 files changed, 84 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page
stash@{1}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page
stash@{2}: WIP on dev: 82e9f14 created index.txt page and renamed it to index.html page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ ^C

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash apply stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git reset --hard
HEAD is now at d6c80f0 popped home and about stashes






BUNDLE 2