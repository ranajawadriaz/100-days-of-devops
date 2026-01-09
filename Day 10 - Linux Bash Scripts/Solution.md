<pre>
thor@jumphost ~$ ssh banner@stapp03
The authenticity of host 'stapp03 (172.16.238.12)' can't be established.
ED25519 key fingerprint is SHA256:TkuITNVkNdnMhwqw8CpDOXE2ymCj8vWSZOdJMWkt6Gc.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp03' (ED25519) to the list of known hosts.
banner@stapp03's password: 
[banner@stapp03 ~]$ sudo yum install zip -y

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for banner: 
Last metadata expiration check: 0:23:53 ago on Fri Jan  9 18:03:13 2026.
Dependencies resolved.
===============================================================================
 Package         Architecture     Version               Repository        Size
===============================================================================
Installing:
 zip             x86_64           3.0-35.el9            baseos           266 k
Installing dependencies:
 unzip           x86_64           6.0-59.el9            baseos           182 k

Transaction Summary
===============================================================================
Install  2 Packages

Total download size: 447 k
Installed size: 1.1 M
Downloading Packages:
(1/2): unzip-6.0-59.el9.x86_64.rpm             1.9 MB/s | 182 kB     00:00    
(2/2): zip-3.0-35.el9.x86_64.rpm               2.7 MB/s | 266 kB     00:00    
-------------------------------------------------------------------------------
Total                                          1.3 MB/s | 447 kB     00:00     
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                       1/1 
  Installing       : unzip-6.0-59.el9.x86_64                               1/2 
  Installing       : zip-3.0-35.el9.x86_64                                 2/2 
  Running scriptlet: zip-3.0-35.el9.x86_64                                 2/2 
  Verifying        : unzip-6.0-59.el9.x86_64                               1/2 
  Verifying        : zip-3.0-35.el9.x86_64                                 2/2 

Installed:
  unzip-6.0-59.el9.x86_64                 zip-3.0-35.el9.x86_64                

Complete!
[banner@stapp03 ~]$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/banner/.ssh/id_rsa): 
Created directory '/home/banner/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/banner/.ssh/id_rsa
Your public key has been saved in /home/banner/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:+uyuJyZumzFY3JMmawYJvfMeYeoOnEWtmMAEnUTHYN8 banner@stapp03.stratos.xfusioncorp.com
The key's randomart image is:
+---[RSA 3072]----+
|o==+.            |
|ooooo.           |
|o.....E          |
|..++.. .         |
| o=o* = S        |
|. oO = o         |
|.oo O .          |
| o +o=oo.        |
| .oo=+.*=        |
+----[SHA256]-----+
[banner@stapp03 ~]$ ssh-copy-id clint@stbkp01
/usr/bin/ssh-copy-id: INFO: Source of key(s) to be installed: "/home/banner/.ssh/id_rsa.pub"
The authenticity of host 'stbkp01 (172.16.238.16)' can't be established.
ED25519 key fingerprint is SHA256:XbrPJNZ7l5ePXrApBF1Hh7op2n4YTu6yaPVtdGMD+/U.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
/usr/bin/ssh-copy-id: INFO: attempting to log in with the new key(s), to filter out any that are already installed
/usr/bin/ssh-copy-id: INFO: 1 key(s) remain to be installed -- if you are prompted now it is to install the new keys
clint@stbkp01's password: 

Number of key(s) added: 1

Now try logging into the machine, with:   "ssh 'clint@stbkp01'"
and check to make sure that only the key(s) you wanted were added.

[banner@stapp03 ~]$ ssh clint@stbkp01
[clint@stbkp01 ~]$ exit
logout
Connection to stbkp01 closed.
[banner@stapp03 ~]$ vi /scripts/news_backup.sh
[banner@stapp03 ~]$ chmod +x /scripts/news_backup.sh
[banner@stapp03 ~]$ ./scripts/news_backup.sh
-bash: ./scripts/news_backup.sh: No such file or directory
[banner@stapp03 ~]$ ls -l /backup/
total 0
[banner@stapp03 ~]$ vi /scripts/news_backup.sh
[banner@stapp03 ~]$ ./scripts/news_backup.sh
-bash: ./scripts/news_backup.sh: No such file or directory
[banner@stapp03 ~]$
</pre>