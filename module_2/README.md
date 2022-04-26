
````
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

PS C:\Users\reinist\git_repos\DevOpsHomeWork> cd ..
PS C:\Users\reinist\git_repos> git clone git@github.com:hashicorp/terraform.git
Cloning into 'terraform'...
remote: Enumerating objects: 258425, done.
remote: Counting objects: 100% (45/45), done.
remote: Compressing objects: 100% (27/27), done.
remote: Total 258425 (delta 24), reused 31 (delta 18), pack-reused 258380
Receiving objects: 100% (258425/258425), 190.53 MiB | 3.95 MiB/s, done.

Resolving deltas: 100% (160492/160492), done.
Updating files: 100% (3057/3057), done.
PS C:\Users\reinist\git_repos> cd .\terraform\


PS C:\Users\reinist\git_repos\DevOpsHomeWork> git ls-tree -r HEAD --l
100644 blob 155581934185fbccf36a2f0c5514b6f636ae48a4      39    HelloWorld.sh
100644 blob 6ab6be0d8479e2bcb4dd0a1e7d66b9d69f6d8755      32    module_1/README.md
100644 blob 2fbd83ae8cbc0ec30972419f27bf3f340c895a5e   29253    module_1/img/image.png
100644 blob 2fbd83ae8cbc0ec30972419f27bf3f340c895a5e   29253    module_2/img/image.png
PS C:\Users\reinist\git_repos\DevOpsHomeWork>

PS C:\Users\reinist\git_repos\terraform> git log --since='2021-04-01' --until='2021-05-1' --grep="Laura Pacilio"
PS C:\Users\reinist\git_repos\terraform> git log --since='2022-04-25' --until='2022-04-26' --grep="Laura Pacilio"
PS C:\Users\reinist\git_repos\terraform> git log --since='2022-04-01' --until='2022-04-26' --grep="Laura Pacilio"
commit 8138fb7b292ad3a48bf3001458e495af9cc98826
Author: Brandon Croft <brandon.croft@gmail.com>
Date:   Wed Apr 13 13:48:17 2022 -0600

    Apply suggestions from documentation review

    Co-authored-by: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>

commit dff6a8431ce0d0e391dcb1352f16ba7964793cfb
Author: Brandon Croft <brandon.croft@gmail.com>
Date:   Tue Apr 5 13:23:46 2022 -0600

    Apply doc suggestions from code review

    Co-authored-by: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>

commit f95c7935c9706ff4a7c1b21e460f6491c7e210b6 (origin/sebasslash/tf-workspace-cloud-config)
Author: Sebastian Rivera <sebastian.rivera@hashicorp.com>
Date:   Mon Apr 11 14:33:13 2022 -0400

    Update website/docs/cli/cloud/settings.mdx

    Co-authored-by: Laura Pacilio <83350965+laurapacilio@users.noreply.github.com>
PS C:\Users\reinist\git_repos\terraform>


PS C:\Users\reinist\git_repos\terraform> git log --since='2021-04-20' --until='2021-04-21'
commit f8493bf5cd78bc2a723f5ddc6f6bceb0e08813ea
Author: James Bardin <j.bardin@gmail.com>
Date:   Fri Apr 16 17:11:27 2021 -0400

    update hcl

    update to v2.10.0

commit d15f7394a19f8f4d604b632df54c1d0cc0c9cc85
Merge: fabdf0bea 7f571b5eb
Author: James Bardin <j.bardin@gmail.com>
Date:   Tue Apr 20 16:25:34 2021 -0400

    Merge pull request #28457 from hashicorp/jbardin/provisioner-null-checks

    additional null checks in provisioners

commit 7f571b5ebb76111a2c671ac0c2212379cc676bcd
Author: James Bardin <j.bardin@gmail.com>
Date:   Tue Apr 20 12:31:32 2021 -0400

    additional null checks in provisioners

    Now that provisioners for directly with the plugin API and cty data
    types, we need to add a few null checks to catch invalid input that
    would have otherwise been masked by the legacy SDK.

commit fabdf0bea1fa2bf6a9d56cc3ea0f28242bf5e812
Author: John Houston <jrhouston@users.noreply.github.com>
Date:   Tue Apr 20 10:05:45 2021 -0400

    Add config_paths and drop KUBECONFIG env variable in kubernetes backend (#26997)

````


Atbilde uz pedejo jautajumu: Es domaju tas tapec ka bija lokals commit, bet nopushots tika velak.
