<pre>
thor@jumphost ~$ ssh tony@stapp01
The authenticity of host 'stapp01 (172.16.238.10)' can't be established.
ED25519 key fingerprint is SHA256:NFgLdgxaB3kp5fpg64MHZtEHcwfuuQNIfMRk+ezaF4E.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stapp01' (ED25519) to the list of known hosts.
tony@stapp01's password: 
[tony@stapp01 ~]$ ls -l /tmp/xfusioncorp.sh
---------- 1 root root 40 Sep  9 20:30 /tmp/xfusioncorp.sh
[tony@stapp01 ~]$ sudo chmod a+rx /tmp/xfusioncorp.sh

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for tony: 
[tony@stapp01 ~]$ ls -l /tmp/xfusioncorp.sh
-r-xr-xr-x 1 root root 40 Sep  9 20:30 /tmp/xfusioncorp.sh
[tony@stapp01 ~]$ /tmp/xfusioncorp.sh
Welcome To KodeKloud
[tony@stapp01 ~]$ cat /tmp/xfusioncorp.sh
#!/bin/bash

echo "Welcome To KodeKloud"[tony@stapp01 ~]$
</pre>