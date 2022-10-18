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