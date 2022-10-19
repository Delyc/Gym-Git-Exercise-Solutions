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
















#Exercise 2

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git checkout dev
Switched to branch 'dev'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git pull ft/bundle-2
fatal: 'ft/bundle-2' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git pull origin ft/bundle-2
From https://github.com/Delyc/Gym-Git-Exercise-Solutions
 * branch            ft/bundle-2 -> FETCH_HEAD
Updating 82e9f14..9ceb85e
Fast-forward
 README.md     | 170 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 about.html    |  12 +++++
 home.html     |  12 +++++
 services.html |  12 +++++
 4 files changed, 205 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "redesigned service page"
[ft/service-redesign 33792f9] redesigned service page
 1 file changed, 1 insertion(+)

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 347 bytes | 347.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Delyc/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git commit -m "updated services page"
[main d70eeae] updated services page
 1 file changed, 1 insertion(+), 1 deletion(-)

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 309 bytes | 309.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
   759a97a..d70eeae  main -> main

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff --color-words

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff origin/main ft/service-redesign
diff --git a/services.html b/services.html
index f6603d6..398ae33 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,7 @@
     <title>Document</title>
 </head>
 <body>
-    <h1>This is the service page, updated</h1>
+    <h1>This is the service page, from services-redesign</h1>
+    <p>I am updated from another branch</p>
 </body>
 </html>
\ No newline at end of file

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge origin main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git commit -m "merged from main"
[ft/service-redesign cd0a262] merged from main

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 346 bytes | 346.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
   511a1d1..cd0a262  ft/service-redesign -> ft/service-redesign

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
