---
title: LazyAdmin
premalink: "/lazyAdmin"
---

# **LAzY ADmIn**


## Open Ports:
  - 21: ssh
  - 80: HTTP
  
## Port 80:
1. find sub-doamisn and directories usind **dirb**
   - ip/content **(we find sweetrice)**
   - ip/content/as **(login Page)**
   - ip/content/inc/mysqlbackup **(found username and password)**
![mysqlbackup.png](images/lazyAdmin/mysqlbackup.png)
   
## Gaining Access:
 **SweetRice has a _Remote_ _Code_ _Execution_ vulnerablitiy**
 - Uploading a **php reverse shell** in themes 
 - listening via netcat will gain you access to the **BOX**
### USER Flag:
![user_flag](images/lazyAdmin/user_flag.png)
 


## Privilege Escalation:
 - sudo -l
    - This will show about things you can run as **sudo**
    - On tracing the flie Paths we find we can edit _/etc/copy.sh_
    
    **Edit the IP and the PORT**
 - Executing the file and listening to it  via netcat will give to root access
### Root Flag:
![rootflag.png](images/lazyAdmin/root.flag.png)
