<pre>
thor@jumphost ~$ ^C
thor@jumphost ~$ ssh peter@stdb01
The authenticity of host 'stdb01 (172.16.239.10)' can't be established.
ED25519 key fingerprint is SHA256:ZrAUe2zbqjEr9a5H5ppb2bfFR6SVz6EB+oPfAKEJLeo.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'stdb01' (ED25519) to the list of known hosts.
peter@stdb01's password: 
[peter@stdb01 ~]$ sudo systemctl status mariadb

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for peter: 
○ mariadb.service - MariaDB 10.5 database server
     Loaded: loaded (/usr/lib/systemd/system/mariadb.service; enabled; preset: disabled)
     Active: inactive (dead) since Thu 2026-01-08 16:12:53 UTC; 12min ago
   Duration: 6.255s
       Docs: man:mariadbd(8)
             https://mariadb.com/kb/en/library/systemd/
    Process: 879 ExecStartPre=/usr/libexec/mariadb-check-socket (code=exited, status=0/SUCCESS)
    Process: 1086 ExecStartPre=/usr/libexec/mariadb-prepare-db-dir mariadb.service (code=exited, status=0/SUCCESS)
    Process: 1447 ExecStart=/usr/libexec/mariadbd --basedir=/usr $MYSQLD_OPTS $_WSREP_NEW_CLUSTER (code=exited, status=0/SUCCESS)
    Process: 1497 ExecStartPost=/usr/libexec/mariadb-check-upgrade (code=exited, status=0/SUCCESS)
   Main PID: 1447 (code=exited, status=0/SUCCESS)
     Status: "MariaDB server is down"

Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Got notification message from PID 1447 (STATUS=Free innodb buffer pool, EXTEND_TIMEOUT_USEC=30000000)
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Got notification message from PID 1447 (STATUS=MariaDB server is down)
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Got notification message from PID 1447 (STATUS=MariaDB server is down)
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Child 1447 belongs to mariadb.service.
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Main process exited, code=exited, status=0/SUCCESS (success)
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Deactivated successfully.
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Service restart not allowed.
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Changed stop-sigterm -> dead
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Job 112 mariadb.service/stop finished, result=done
Jan 08 16:12:53 stdb01.stratos.xfusioncorp.com systemd[1]: Stopped MariaDB 10.5 database server.
[peter@stdb01 ~]$ sudo systemctl start mariadb
Job for mariadb.service failed because the control process exited with error code.
See "systemctl status mariadb.service" and "journalctl -xeu mariadb.service" for details.
[peter@stdb01 ~]$ ^C
[peter@stdb01 ~]$ df -h
Filesystem      Size  Used Avail Use% Mounted on
overlay         1.5T  176G  1.2T  13% /
tmpfs            32G     0   32G   0% /proc/acpi
devtmpfs         32G     0   32G   0% /dev/tty
tmpfs            32G     0   32G   0% /proc/scsi
tmpfs            64M     0   64M   0% /dev
shm              64M     0   64M   0% /dev/shm
/dev/md127      1.5T  176G  1.2T  13% /etc/hosts
tmpfs           4.0M     0  4.0M   0% /sys/fs/cgroup
tmpfs            13G  8.1M   13G   1% /run
tmpfs           6.3G     0  6.3G   0% /run/user/1001
[peter@stdb01 ~]$ ls /var/lib/mysql/mysql
ls: cannot access '/var/lib/mysql/mysql': No such file or directory
[peter@stdb01 ~]$ sudo mysql_install_db --user=mysql --datadir=/var/lib/mysql
[sudo] password for peter: 
Installing MariaDB/MySQL system tables in '/var/lib/mysql' ...
OK

To start mariadbd at boot time you have to copy
support-files/mariadb.service to the right place for your system


Two all-privilege accounts were created.
One is root@localhost, it has no password, but you need to
be system 'root' user to connect. Use, for example, sudo mysql
The second is mysql@localhost, it has no password either, but
you need to be the system 'mysql' user to connect.
After connecting you can set the password, if you would need to be
able to connect as any of these users with a password and without sudo

See the MariaDB Knowledgebase at https://mariadb.com/kb

You can start the MariaDB daemon with:
cd '/usr' ; /usr/bin/mariadbd-safe --datadir='/var/lib/mysql'

You can test the MariaDB daemon with mysql-test-run.pl
cd '/usr/share/mysql-test' ; perl mariadb-test-run.pl

Please report any problems at https://mariadb.org/jira

The latest information about MariaDB is available at https://mariadb.org/.

Consider joining MariaDB's strong and vibrant community:
https://mariadb.org/get-involved/

[peter@stdb01 ~]$ sudo systemctl start mariadb
[peter@stdb01 ~]$ sudo systemctl status mariadb
● mariadb.service - MariaDB 10.5 database server
     Loaded: loaded (/usr/lib/systemd/system/mariadb.service; enabled; preset: disabled)
     Active: active (running) since Thu 2026-01-08 16:32:58 UTC; 18s ago
       Docs: man:mariadbd(8)
             https://mariadb.com/kb/en/library/systemd/
    Process: 2575 ExecStartPre=/usr/libexec/mariadb-check-socket (code=exited, status=0/SUCCESS)
    Process: 2609 ExecStartPre=/usr/libexec/mariadb-prepare-db-dir mariadb.service (code=exited, status=0/SUCCESS)
    Process: 2742 ExecStartPost=/usr/libexec/mariadb-check-upgrade (code=exited, status=0/SUCCESS)
   Main PID: 2704 (mariadbd)
     Status: "Taking your SQL requests now..."
      Tasks: 19 (limit: 411434)
     Memory: 62.7M
     CGroup: /docker/e595aae6dd504fe2da65d931fb31ee704a62c6801d009143f15da83dce6f9b46/system.slice/mariadb.service
             └─2704 /usr/libexec/mariadbd --basedir=/usr

Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[2742]: Remounted /run/systemd/unit-root/run/systemd/incoming.
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[2742]: Remounted /run/systemd/unit-root/run/credentials.
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[2742]: mariadb.service: Executing: /usr/libexec/mariadb-check-upgrade
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Child 2742 belongs to mariadb.service.
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Control process exited, code=exited, status=0/SUCCESS (success)
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Got final SIGCHLD for state start-post.
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Changed start-post -> running
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Job 282 mariadb.service/start finished, result=done
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: Started MariaDB 10.5 database server.
Jan 08 16:32:58 stdb01.stratos.xfusioncorp.com systemd[1]: mariadb.service: Failed to send unit change signal for mariadb.service: Connection reset by peer
[peter@stdb01 ~]$ 
</pre>