<pre>
[root@stapp01 ~]# yum install tomcat -y
Last metadata expiration check: 0:00:53 ago on Fri Jan  9 19:06:37 2026.
Dependencies resolved.
===============================================================================
 Package                    Arch       Version             Repository     Size
===============================================================================
Installing:
 tomcat                     noarch     1:9.0.87-6.el9      appstream      98 k
Installing dependencies:
 apr                        x86_64     1.7.0-12.el9        appstream     123 k
 ecj                        noarch     1:4.20-17.el9       appstream     1.9 M
 javapackages-tools         noarch     6.4.0-1.el9         appstream      34 k
 tomcat-el-3.0-api          noarch     1:9.0.87-6.el9      appstream     105 k
 tomcat-jsp-2.3-api         noarch     1:9.0.87-6.el9      appstream      72 k
 tomcat-lib                 noarch     1:9.0.87-6.el9      appstream     6.0 M
 tomcat-servlet-4.0-api     noarch     1:9.0.87-6.el9      appstream     284 k
Installing weak dependencies:
 tomcat-native              x86_64     1:1.3.0-1.el9       epel           74 k

Transaction Summary
===============================================================================
Install  9 Packages

Total download size: 8.7 M
Installed size: 11 M
Downloading Packages:
(1/9): javapackages-tools-6.4.0-1.el9.noarch.r  93 kB/s |  34 kB     00:00    
(2/9): apr-1.7.0-12.el9.x86_64.rpm             272 kB/s | 123 kB     00:00    
(3/9): tomcat-el-3.0-api-9.0.87-6.el9.noarch.r 643 kB/s | 105 kB     00:00    
(4/9): tomcat-jsp-2.3-api-9.0.87-6.el9.noarch. 503 kB/s |  72 kB     00:00    
(5/9): tomcat-9.0.87-6.el9.noarch.rpm          248 kB/s |  98 kB     00:00    
(6/9): tomcat-servlet-4.0-api-9.0.87-6.el9.noa 1.2 MB/s | 284 kB     00:00    
(7/9): tomcat-native-1.3.0-1.el9.x86_64.rpm    195 kB/s |  74 kB     00:00    
(8/9): ecj-4.20-17.el9.noarch.rpm              1.2 MB/s | 1.9 MB     00:01    
(9/9): tomcat-lib-9.0.87-6.el9.noarch.rpm      4.4 MB/s | 6.0 MB     00:01    
-------------------------------------------------------------------------------
Total                                          3.2 MB/s | 8.7 MB     00:02     
Extra Packages for Enterprise Linux 9 - x86_64 1.6 MB/s | 1.6 kB     00:00    
Importing GPG key 0x3228467C:
 Userid     : "Fedora (epel9) <epel@fedoraproject.org>"
 Fingerprint: FF8A D134 4597 106E CE81 3B91 8A38 72BF 3228 467C
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-EPEL-9
Key imported successfully
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                       1/1 
  Installing       : tomcat-servlet-4.0-api-1:9.0.87-6.el9.noarch          1/9 
  Running scriptlet: tomcat-servlet-4.0-api-1:9.0.87-6.el9.noarch          1/9 
  Installing       : tomcat-el-3.0-api-1:9.0.87-6.el9.noarch               2/9 
  Running scriptlet: tomcat-el-3.0-api-1:9.0.87-6.el9.noarch               2/9 
  Installing       : javapackages-tools-6.4.0-1.el9.noarch                 3/9 
  Installing       : ecj-1:4.20-17.el9.noarch                              4/9 
  Installing       : tomcat-jsp-2.3-api-1:9.0.87-6.el9.noarch              5/9 
  Running scriptlet: tomcat-jsp-2.3-api-1:9.0.87-6.el9.noarch              5/9 
  Installing       : tomcat-lib-1:9.0.87-6.el9.noarch                      6/9 
  Installing       : apr-1.7.0-12.el9.x86_64                               7/9 
  Installing       : tomcat-native-1:1.3.0-1.el9.x86_64                    8/9 
  Running scriptlet: tomcat-1:9.0.87-6.el9.noarch                          9/9 
  Installing       : tomcat-1:9.0.87-6.el9.noarch                          9/9 
  Running scriptlet: tomcat-1:9.0.87-6.el9.noarch                          9/9 
  Verifying        : apr-1.7.0-12.el9.x86_64                               1/9 
  Verifying        : ecj-1:4.20-17.el9.noarch                              2/9 
  Verifying        : javapackages-tools-6.4.0-1.el9.noarch                 3/9 
  Verifying        : tomcat-1:9.0.87-6.el9.noarch                          4/9 
  Verifying        : tomcat-el-3.0-api-1:9.0.87-6.el9.noarch               5/9 
  Verifying        : tomcat-jsp-2.3-api-1:9.0.87-6.el9.noarch              6/9 
  Verifying        : tomcat-lib-1:9.0.87-6.el9.noarch                      7/9 
  Verifying        : tomcat-servlet-4.0-api-1:9.0.87-6.el9.noarch          8/9 
  Verifying        : tomcat-native-1:1.3.0-1.el9.x86_64                    9/9 

Installed:
  apr-1.7.0-12.el9.x86_64                                                      
  ecj-1:4.20-17.el9.noarch                                                     
  javapackages-tools-6.4.0-1.el9.noarch                                        
  tomcat-1:9.0.87-6.el9.noarch                                                 
  tomcat-el-3.0-api-1:9.0.87-6.el9.noarch                                      
  tomcat-jsp-2.3-api-1:9.0.87-6.el9.noarch                                     
  tomcat-lib-1:9.0.87-6.el9.noarch                                             
  tomcat-native-1:1.3.0-1.el9.x86_64                                           
  tomcat-servlet-4.0-api-1:9.0.87-6.el9.noarch                                 

Complete!
[root@stapp01 ~]# vi etc/tomcat/server.xml
[root@stapp01 ~]# vi etc/tomcat/server.xml
[root@stapp01 ~]# vi /etc/tomcat/server.xml
[root@stapp01 ~]# rm -rf /var/lib/tomcat/webapps/ROOT
[root@stapp01 ~]# mv /tmp/ROOT.war /var/lib/tomcat/webapps/
[root@stapp01 ~]# systemctl start tomcat
[root@stapp01 ~]# systemctl enable tomcat
Created symlink /etc/systemd/system/multi-user.target.wants/tomcat.service → /usr/lib/systemd/system/tomcat.service.
[root@stapp01 ~]# netstat -tulnp | grep 8089
tcp        0      0 0.0.0.0:8089            0.0.0.0:*               LISTEN      6146/java           
[root@stapp01 ~]# curl http:stapp01:8089
curl: (3) URL using bad/illegal format or missing URL
[root@stapp01 ~]# curl http://stapp01:8089
<!DOCTYPE html>
<!--
To change this license header, choose License Headers in Project Properties.
To change this template file, choose Tools | Templates
and open the template in the editor.
-->
<html>
    <head>
        <title>SampleWebApp</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
        <h2>Welcome to xFusionCorp Industries!</h2>
        <br>
    
    </body>
</html>
[root@stapp01 ~]# ^C
[root@stapp01 ~]#
</pre>