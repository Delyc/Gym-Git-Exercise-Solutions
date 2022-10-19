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




Exercise 2


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ touch team.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m "created team page"
[ft/team-page eabba23] created team page
 2 files changed, 172 insertions(+), 1 deletion(-)
 create mode 100644 team.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 2.31 KiB | 1.15 MiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Delyc/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit eabba234e74b3922f44d435b7b02f11f1cbfdffd (HEAD -> ft/team-page, origin/ft/team-page)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Wed Oct 19 14:38:22 2022 +0200

    created team page

commit cd0a2628a1075641902c9e5b5e3351616190075f (origin/ft/service-redesign, ft/service-redesign)
Merge: 511a1d1 d70eeae
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Wed Oct 19 14:33:09 2022 +0200

    merged from main

commit d70eeaebc445b12e493ab0508c1edd9644289dc2 (origin/main, origin/HEAD, main, ft/contact-page)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Wed Oct 19 14:26:50 2022 +0200

    updated services page

commit 511a1d1f1201d12c71ebe38a73f04d12fab790b3
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Wed Oct 19 14:25:19 2022 +0200

    redesigned service page

commit 759a97afed1276d3f20f31f320673355c5850820
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Wed Oct 19 14:22:48 2022 +0200

    updated services again

commit 33792f96ef8349f9b02ca120238afeb9adeab51d
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Wed Oct 19 14:19:11 2022 +0200

    redesigned service page

commit 9ceb85e502f1e487aadbc2a27403a773f5da6651 (origin/ft/bundle-2, ft/bundle-2)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit
(END)
)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit
(END)
)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit
(END)
)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit
(END)
)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit
(END)
)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit
(END)
)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 14:17:28 2022 +0200

    created services page

commit d6c80f0bbc79b952ab8958b090b85377aac9bdc4 (dev)
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:30:59 2022 +0200

    popped home and about stashes

commit 82e9f14514f38418056f784d0eadb91aef459715
Author: Delyc <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:20:30 2022 +0200

    created index.txt page and renamed it to index.html page

commit 708dc8c73da9a5fa8a45c77839782bedf032c14e
Author: Delyce Twizeyimana <d.twizeyima@alustudent.com>
Date:   Tue Oct 18 13:15:58 2022 +0200

    Initial commit

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick eabba234e74b3922f44d435b7b02f11f1cbfdffd
[ft/contact-page 9fb3bc4] created team page
 Date: Wed Oct 19 14:38:22 2022 +0200
 2 files changed, 172 insertions(+), 1 deletion(-)
 create mode 100644 team.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m "added content to the home page"
[ft/contact-page da33472] added content to the home page
 1 file changed, 12 insertions(+)
 create mode 100644 contact.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ ^C

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ ^[[200~  git push --set-upstream origin ft/contact-page
bash: $'\E[200~': command not found

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$   git push --set-upstream origin ft/contact-page
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 2.67 KiB | 1.34 MiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Delyc/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ touch faq.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "created faq page"
[ft/faq-page 818583d] created faq page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$   git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 471 bytes | 471.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Delyc/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ ^C

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert eabba234e74b3922f44d435b7b02f11f1cbfdffd
[ft/faq-page fe41b92] revert "created team page"
 2 files changed, 1 insertion(+), 172 deletions(-)
 delete mode 100644 team.html

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 522 bytes | 522.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Delyc/Gym-Git-Exercise-Solutions.git
   818583d..fe41b92  ft/faq-page -> ft/faq-page

TheGym@DESKTOP-NLLQJTO MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/faq-page)
