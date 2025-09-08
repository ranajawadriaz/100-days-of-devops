<pre>
thor@jumphost ~$ ssh tony@stapp01
The authenticity of host 'stapp01 (172.16.238.10)' can't be established.
ED25519 key fingerprint is SHA256:GJjWDnTflhBhOjujOUiMJMBupV+id3WuDYR+p6ATKmU.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp01' (ED25519) to the list of known hosts.
tony@stapp01's password: 
[tony@stapp01 ~]$ sudo vi /etc/ssh/sshd_config

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for tony: 
[tony@stapp01 ~]$ sudo systemctl restart sshd
[tony@stapp01 ~]$ ssh thor@jumphost
ssh: Could not resolve hostname jumphost: Name or service not known
[tony@stapp01 ~]$ ssh tony@stapp01
The authenticity of host 'stapp01 (172.16.238.10)' can't be established.
ED25519 key fingerprint is SHA256:GJjWDnTflhBhOjujOUiMJMBupV+id3WuDYR+p6ATKmU.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp01' (ED25519) to the list of known hosts.
tony@stapp01's password: 
Last login: Mon Sep  8 15:57:04 2025 from 172.16.238.2
[tony@stapp01 ~]$ exit
logout
Connection to stapp01 closed.
[tony@stapp01 ~]$ ^C
[tony@stapp01 ~]$ ssh tony@stapp01
tony@stapp01's password: 
Last login: Mon Sep  8 16:03:12 2025 from 172.16.238.10
[tony@stapp01 ~]$ exit
logout
Connection to stapp01 closed.
[tony@stapp01 ~]$ ssh root@stapp01
root@stapp01's password: 
Permission denied, please try again.
root@stapp01's password: 

[tony@stapp01 ~]$ ssh root@stapp02
The authenticity of host 'stapp02 (172.16.238.11)' can't be established.
ED25519 key fingerprint is SHA256:vJivAPAgmHCEoM9pCgm1zuJApOg2XOO+QYP7GkC6R5M.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp02' (ED25519) to the list of known hosts.
root@stapp02's password: 
Permission denied, please try again.
root@stapp02's password: 

[tony@stapp01 ~]$ ssh steve@stapp02
steve@stapp02's password: 
[steve@stapp02 ~]$ sudo vi /etc/ssh/sshd_config

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for steve: 
[steve@stapp02 ~]$ sudo passwd -S root
[sudo] password for steve: 
root PS 2025-08-29 0 99999 7 -1 (Password set, SHA512 crypt.)
[steve@stapp02 ~]$ exit
logout
Connection to stapp02 closed.
[tony@stapp01 ~]$ ssh tony@stapp01
tony@stapp01's password: 
Last login: Mon Sep  8 16:04:28 2025 from 172.16.238.10
[tony@stapp01 ~]$ sudo passwd -S root
[sudo] password for tony: 
root PS 2025-08-29 0 99999 7 -1 (Password set, SHA512 crypt.)
[tony@stapp01 ~]$ exit
logout
Connection to stapp01 closed.
[tony@stapp01 ~]$ ssh steve@stapp02
steve@stapp02's password: 
Last login: Mon Sep  8 16:08:05 2025 from 172.16.238.10
[steve@stapp02 ~]$ sudo vi /etc/ssh/sshd_config
[sudo] password for steve: 
[steve@stapp02 ~]$ sudo systemctl restart sshd
[steve@stapp02 ~]$ exit
logout
Connection to stapp02 closed.
[tony@stapp01 ~]$ ssh banner@stapp03
The authenticity of host 'stapp03 (172.16.238.12)' can't be established.
ED25519 key fingerprint is SHA256:yQXMINls9jSSSRuZmi4DdXIW3Uu0om2MIx0BFSK1bQY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp03' (ED25519) to the list of known hosts.
banner@stapp03's password: 
[banner@stapp03 ~]$ sudo vi /etc/ssh/sshd_config

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for banner: 
[banner@stapp03 ~]$ sudo systemctl restart sshd
[banner@stapp03 ~]$ exit
logout
Connection to stapp03 closed.
[tony@stapp01 ~]$ 
</pre>