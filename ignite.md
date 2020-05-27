---
title: Ignite
premalink: /ignite
---
# ![front](saharshtapi.github.io/images/ignite/front.png)
[https://tryhackme.com/room/ignite](https://tryhackme.com/room/ignite)

## Open Ports:
  - 80: HTTP
     - It has Remote Code Exec Vul
     - Fuel CMS 1.4
  
## Port 80:
![login](saharshtapi.github.io/images/ignite/login.png)
   
## Gaining Access:
 1. Download the Python file  from exploit-db (feul cms 1.4.1)
  - Change the ip and the port
  - Remove proxy 
  > Python exploit.py

### USER Flag:
![user_flag](saharshtapi.github.io/images/ignite/USER.png)
 
## Privilege Escalation:
 1. Go to database.php i.e
 > cd var/html/www/fuel/application/config/database.php
![databse](saharshtapi.github.io/images/ignite/database.png)
 > cat database.php
![user_flag](saharshtapi.github.io/images/ignite/rootpass.png)
 2. Now convert your shell to tty
 > python -c 'import pty; pty.spawn("/bin/sh")'
 > su(**and then the passwd**)

### Root Flag:
![rootflag.png](saharshtapi.github.io/images/ignite/ROOT.png)
