<pre>
thor@jumphost ~$ ssh tony@stapp01
The authenticity of host 'stapp01 (172.16.238.10)' can't be established.
ED25519 key fingerprint is SHA256:2gxFIVvOMJswWm3lqcjGQSo8hG+5NU4+FpXV08rPFb4.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp01' (ED25519) to the list of known hosts.
tony@stapp01's password: 
[tony@stapp01 ~]$ sudo chage -l rose

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for tony: 
chage: user 'rose' does not exist in /etc/passwd
[tony@stapp01 ~]$ sudo useradd -e 2024-04-15 rose
[tony@stapp01 ~]$ sudo chage -l rose
Last password change                                    : Sep 07, 2025
Password expires                                        : never
Password inactive                                       : never
Account expires                                         : Apr 15, 2024
Minimum number of days between password change          : 0
Maximum number of days between password change          : 99999
Number of days of warning before password expires       : 7
[tony@stapp01 ~]$ 
</pre>