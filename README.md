Git_test
==========
  # Creating a repository

  * vagrant@precise32:~$ pwd
   /home/vagrant
  * vagrant@precise32:~$ mkdir git_test
  * vagrant@precise32:~$ cd git_test
  * vagrant@precise32:~/git_test$ 
  * vagrant@precise32:~/git_test$ git init
   Reinitialized existing Git repository in /home/vagrant/git_test/.git/
          On Terminal
   Sotirioss-MacBook-Pro:~ sotiri$ pwd
   /Users/sotiri
   * Sotirioss-MacBook-Pro:~ sotiri$ cd bloc-vagrant
   * Sotirioss-MacBook-Pro:bloc-vagrant sotiri$ cd git_test
   * Sotirioss-MacBook-Pro:git_test sotiri$ ls -l
     total 8
     -rw-r--r--  1 sotiri  staff  152 Oct 20 14:50 readme.txt
   Sotirioss-MacBook-Pro:git_test sotiri$ 
   
   
   
   
   
   
   
   vagrant@precise32:~/git_test$ touch readme.txt
vagrant@precise32:~/git_test$ 



Welcome to your Vagrant-built virtual machine.
Last login: Mon Oct 20 13:50:43 2014 from 10.0.2.2
vagrant@precise32:~$ pwd
/home/vagrant
vagrant@precise32:~$ cd git_test
vagrant@precise32:~/git_test$ ls -al
total 12
drwxrwxr-x  3 vagrant vagrant 4096 Oct 21 00:01 .
drwxr-xr-x 17 vagrant vagrant 4096 Oct 20 23:47 ..
drwxrwxr-x  7 vagrant vagrant 4096 Oct 20 23:49 .git
-rw-rw-r--  1 vagrant vagrant    0 Oct 21 00:01 readme.txt
vagrant@precise32:~/git_test$ touch readme.txt
vagrant@precise32:~/git_test$ ls -al
total 12
drwxrwxr-x  3 vagrant vagrant 4096 Oct 21 00:01 .
drwxr-xr-x 17 vagrant vagrant 4096 Oct 20 23:47 ..
drwxrwxr-x  7 vagrant vagrant 4096 Oct 20 23:49 .git
-rw-rw-r--  1 vagrant vagrant    0 Oct 21 00:14 readme.txt
vagrant@precise32:~/git_test$ ls -al
total 12
drwxrwxr-x  3 vagrant vagrant 4096 Oct 21 00:01 .
drwxr-xr-x 17 vagrant vagrant 4096 Oct 20 23:47 ..
drwxrwxr-x  7 vagrant vagrant 4096 Oct 20 23:49 .git
-rw-rw-r--  1 vagrant vagrant    0 Oct 21 00:14 readme.txt


vagrant@precise32:~/git_test$ ls -al
total 16
drwxrwxr-x  3 vagrant vagrant 4096 Oct 21 00:01 .
drwxr-xr-x 17 vagrant vagrant 4096 Oct 20 23:47 ..
drwxrwxr-x  7 vagrant vagrant 4096 Oct 20 23:49 .git
-rw-rw-r--  1 vagrant vagrant   63 Oct 21 00:29 readme.txt

vagrant@precise32:~/git_test$ git status
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#	readme.txt
nothing added to commit but untracked files present (use "git add" to track)
vagrant@precise32:~/git_test$ git add readme.txt
vagrant@precise32:~/git_test$ git status
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#	new file:   readme.txt
#
vagrant@precise32:~/git_test$ git commit -m 'first commit'
[master (root-commit) 1097903] first commit
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
vagrant@precise32:~/git_test$ nano readme.txt
vagrant@precise32:~/git_test$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#	modified:   readme.txt
#
no changes added to commit (use "git add" and/or "git commit -a")
vagrant@precise32:~/git_test$ git diff
diff --git a/readme.txt b/readme.txt
index 228aba4..70ed197 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1,2 +1,4 @@
 This is the first line of text
 This is the second line of text
+This is the third line of text
+This is the fourth line of text
vagrant@precise32:~/git_test$ 
vagrant@precise32:~/git_test$ git add .
vagrant@precise32:~/git_test$ git commit -m 'second commit'
[master 9054348] second commit
 1 file changed, 2 insertions(+)
vagrant@precise32:~/git_test$ git log
commit 9054348d99fe07756156e755a5803af18226733b
Author: Sotirios Dayanis <sotirios.dayanis@gmail.com>
Date:   Tue Oct 21 00:44:28 2014 +0000

    second commit

commit 10979037ac4f4feee2685822d46b114b5dabfad1
Author: Sotirios Dayanis <sotirios.dayanis@gmail.com>
Date:   Tue Oct 21 00:37:56 2014 +0000

    first commit
vagrant@precise32:~/git_test$ 
