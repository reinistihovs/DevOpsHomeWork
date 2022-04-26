
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


Atbilde uz pedejo jautajumu:
Palasot informaciju seit:
https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/troubleshooting-commits-on-your-timeline

izspriedu ka author date atskiras no commit date

PS C:\Users\reinist\git_repos\terraform> git show f8493bf5cd78bc2a723f5ddc6f6bceb0e08813ea --pretty=fuller
commit f8493bf5cd78bc2a723f5ddc6f6bceb0e08813ea
Author:     James Bardin <j.bardin@gmail.com>
AuthorDate: Fri Apr 16 17:11:27 2021 -0400
Commit:     James Bardin <j.bardin@gmail.com>
CommitDate: Tue Apr 20 17:04:56 2021 -0400

    update hcl

    update to v2.10.0

diff --git a/go.mod b/go.mod
index 752fa0f6f..7d278f4ae 100644
--- a/go.mod
+++ b/go.mod
@@ -65,7 +65,7 @@ require (
        github.com/hashicorp/go-uuid v1.0.1
        github.com/hashicorp/go-version v1.2.1
        github.com/hashicorp/hcl v0.0.0-20170504190234-a4b07c25de5f
-       github.com/hashicorp/hcl/v2 v2.9.1
+       github.com/hashicorp/hcl/v2 v2.10.0
        github.com/hashicorp/memberlist v0.1.0 // indirect
        github.com/hashicorp/serf v0.0.0-20160124182025-e4ec8cc423bb // indirect
        github.com/hashicorp/terraform-config-inspect v0.0.0-20210209133302-4fd17a0faac2
diff --git a/go.sum b/go.sum
index f54a79334..6e92bf4cc 100644
--- a/go.sum
+++ b/go.sum
@@ -318,8 +318,6 @@ github.com/hashicorp/go-checkpoint v0.5.0/go.mod h1:7nfLNL10NsxqO4iWuW6tWW0HjZuD
 github.com/hashicorp/go-cleanhttp v0.5.0/go.mod h1:JpRdi6/HCYpAwUzNwuwqhbovhLtngrth3wmdIIUrZ80=
 github.com/hashicorp/go-cleanhttp v0.5.1 h1:dH3aiDG9Jvb5r5+bYHsikaOUIpcM0xvgMXVoDkXMzJM=
 github.com/hashicorp/go-cleanhttp v0.5.1/go.mod h1:JpRdi6/HCYpAwUzNwuwqhbovhLtngrth3wmdIIUrZ80=
-github.com/hashicorp/go-getter v1.5.1 h1:lM9sM02nvEApQGFgkXxWbhfqtyN+AyhQmi+MaMdBDOI=
-github.com/hashicorp/go-getter v1.5.1/go.mod h1:a7z7NPPfNQpJWcn4rSWFtdrSldqLdLPEF3d8nFMsSLM=
 github.com/hashicorp/go-getter v1.5.2 h1:XDo8LiAcDisiqZdv0TKgz+HtX3WN7zA2JD1R1tjsabE=
 github.com/hashicorp/go-getter v1.5.2/go.mod h1:orNH3BTYLu/fIxGIdLjLoAJHWMDQ/UKQr5O4m3iBuoo=
 github.com/hashicorp/go-hclog v0.14.1/go.mod h1:whpDNt7SSdeAju8AWKIWsul05p54N/39EeqMAyrmvFQ=
@@ -360,8 +358,8 @@ github.com/hashicorp/golang-lru v0.5.1/go.mod h1:/m3WP610KZHVQ1SGc6re/UDhFvYD7pJ
 github.com/hashicorp/hcl v0.0.0-20170504190234-a4b07c25de5f h1:UdxlrJz4JOnY8W+DbLISwf2B8WXEolNRA8BGCwI9jws=
 github.com/hashicorp/hcl v0.0.0-20170504190234-a4b07c25de5f/go.mod h1:oZtUIOe8dh44I2q6ScRibXws4Ajl+d+nod3AaR9vL5w=
 github.com/hashicorp/hcl/v2 v2.0.0/go.mod h1:oVVDG71tEinNGYCxinCYadcmKU9bglqW9pV3txagJ90=
-github.com/hashicorp/hcl/v2 v2.9.1 h1:eOy4gREY0/ZQHNItlfuEZqtcQbXIxzojlP301hDpnac=
-github.com/hashicorp/hcl/v2 v2.9.1/go.mod h1:FwWsfWEjyV/CMj8s/gqAuiviY72rJ1/oayI9WftqcKg=
+github.com/hashicorp/hcl/v2 v2.10.0 h1:1S1UnuhDGlv3gRFV4+0EdwB+znNP5HmcGbIqwnSCByg=
+github.com/hashicorp/hcl/v2 v2.10.0/go.mod h1:FwWsfWEjyV/CMj8s/gqAuiviY72rJ1/oayI9WftqcKg=
 github.com/hashicorp/memberlist v0.1.0 h1:qSsCiC0WYD39lbSitKNt40e30uorm2Ss/d4JGU1hzH8=
 github.com/hashicorp/memberlist v0.1.0/go.mod h1:ncdBp14cuox2iFOq3kDiquKU6fqsTBc3W6JvZwjxxsE=
 github.com/hashicorp/serf v0.0.0-20160124182025-e4ec8cc423bb h1:ZbgmOQt8DOg796figP87/EFCVx2v2h9yRvwHF/zceX4=
PS C:\Users\reinist\git_repos\terraform>
