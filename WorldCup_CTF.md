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
	* A txt file **"2007.txt"** inside directory y/u/v/r/a/j
	 * It contains hint to some file.



### Port 21(*FTP*)
* found Anonymoous login in **FTP**
	* found *zip* file name  **treasure.zip**
		* 
