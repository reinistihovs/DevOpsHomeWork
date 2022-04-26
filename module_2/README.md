
PS C:\Users\reinist> cd .\git_repos\
PS C:\Users\reinist\git_repos> git clone git@github.com:reinistihovs/DevOpsHomeWork.git
Cloning into 'DevOpsHomeWork'...
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (5/5), done.
Receiving objects: 100% (9/9), done.
remote: Total 9 (delta 0), reused 6 (delta 0), pack-reused 0
PS C:\Users\reinist\git_repos> cd .\DevOpsHomeWork\
PS C:\Users\reinist\git_repos\DevOpsHomeWork> mkdir module_1


    Directory: C:\Users\reinist\git_repos\DevOpsHomeWork


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        26.04.2022     11:37                module_1


PS C:\Users\reinist\git_repos\DevOpsHomeWork> mkdir module_2


    Directory: C:\Users\reinist\git_repos\DevOpsHomeWork


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        26.04.2022     11:37                module_2


PS C:\Users\reinist\git_repos\DevOpsHomeWork> notepad++.exe .\module_1\README.MD

PS C:\Users\reinist\git_repos\DevOpsHomeWork> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    README.md -> module_1/README.md
        new file:   module_1/img/image.png
        new file:   module_2/img/image.png

PS C:\Users\reinist\git_repos\DevOpsHomeWork> git commit -m "first commit"
[main 41919ec] first commit
 3 files changed, 0 insertions(+), 0 deletions(-)
 rename README.md => module_1/README.md (100%)
 create mode 100644 module_1/img/image.png
 create mode 100644 module_2/img/image.png
PS C:\Users\reinist\git_repos\DevOpsHomeWork> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 25.15 KiB | 6.29 MiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:reinistihovs/DevOpsHomeWork.git
   c80f7cf..41919ec  main -> main


PS C:\Users\reinist\git_repos\DevOpsHomeWork> git ls-tree -r HEAD --l
100644 blob 155581934185fbccf36a2f0c5514b6f636ae48a4      39    HelloWorld.sh
100644 blob 6ab6be0d8479e2bcb4dd0a1e7d66b9d69f6d8755      32    module_1/README.md
100644 blob 2fbd83ae8cbc0ec30972419f27bf3f340c895a5e   29253    module_1/img/image.png
100644 blob 2fbd83ae8cbc0ec30972419f27bf3f340c895a5e   29253    module_2/img/image.png
PS C:\Users\reinist\git_repos\DevOpsHomeWork>