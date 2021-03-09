# THM CC: Pen Testing

### In this writeup Today we're going to try to Solve a room in THM called  [CC: Pen Testing](https://tryhackme.com/room/ccpentesting)

## Task 1 
This Section is a Introduction about the room 
 **no answer needed**

## Task 2 (Nmap)
This Section Called Nmap in this Section You Will Use Nmap to Scan  & Recon The Machine
Nmap is one of the most important tools for pentesting, if you don't know Nmap use  **man command in linux** or **you can ask google**

    $ man nmap
![Man Nmap](https://res.cloudinary.com/micro0x00/image/upload/v1615225214/Screenshot_2021-03-08_192242_asg6li.png)
It will show you everything about nmap
#1. **What does nmap stand for ?**
answer : **Network Mapper**
__________________

#2. **How do you specify which port(s) to scan ?**

answer : **-p**
__________________

#3. **How do you do a "ping scan"(just tests if the host(s) is up) ?**

answer: **-sn**
__________________

#4. **What is the flag for a UDP scan ?**

![udp scan flag](https://res.cloudinary.com/micro0x00/image/upload/v1615226720/udp_uoyu1k.png)

answer: **-sU**
__________________

#5. **How do you run default scripts ?**

![default script](https://res.cloudinary.com/micro0x00/image/upload/v1615227012/sc_ied8ds.png)

answer: -**sC**
__________________

#6. **How do you enable "aggressive mode"(Enables OS detection, version detection, script scanning, and traceroute) ?**

![enable aggressive mode](https://res.cloudinary.com/micro0x00/image/upload/v1615227295/_a_ggxvew.png)

answer :  **-A**
__________________
#7. **What flag enables OS detection ?**

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615239877/-O_loldqt.png)

answer : **-O**
_______________________
#8. **How do you get the versions of services running on the target machine**

answer : -sV
_________________________
#9. **Deploy the machine** 

answer : **Deploy the machine (No answer needed )
after that run** `$ nmap -A -sC -sV -O <IP Address>`

![the scan](https://res.cloudinary.com/micro0x00/image/upload/v1615274991/ths_scan_fsxmjf.png)
_____________________________
#10. **How many ports are open on the machine ?**
answer :  **1**
__________________________
#11. **What service is running on the machine ?**

answer : **apache**
______________________________________________
#12. **What is the version of the service ?**
answer : **2.4.18**
________________
#13. **What is the output of the http-title script(included in default scripts) ?**
answer : **Apache2 Ubuntu Default Page: It Works**
____________
## Task 3 (NetCat)
This Section Called NetCat in this Section You Will Use NetCat it's allows users to connect to specific ports and send and receive data
if you don't know it you can use **man command in linux** or **you can ask google**

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615275369/Nc_datqrb.png)
____________________________
#1. ** How do you listen for connections ?**

answer: **-l**
____________________
#2. **How do you enable verbose mode(allows you to see who connected to you) ? **

answer: **-v**
______________
#3. **How do you specify a port to listen on ?**

answer : **-p**
_________________
#4. **How do you specify which program to execute after you connect to a host(One of the most infamous)?**
answer : **-e**
#5. **How do you connect to udp ports ?**

answer **-u**
__________________________
## Task 4 (gobuster)
you can download  gobuster form [here](https://github.com/OJ/gobuster)
gobuster can tell you where some files and directories are; however, some of the more hidden stuff is often hidden away from the eyes of users.
____
#1. **How do you specify directory/file brute forcing mode?**

answer : **dir**
_________
#2. **How do you specify dns bruteforcing mode?**

answer : **dns**
______
#3. **What flag sets extensions to be used ?**

answer : **-x**
_______
#4. **What flag sets a wordlist to be used ?**

answer : **-w**
________
#5. **How do you set the Username for basic authentication ?**

answer : **-u** 
_______
#6. **How do you set the Password for basic authentication ?**

answer : **-p**
___________________
#7. **How do you set which status codes gobuster will interpret as valid ?**

answer : **-s** 
________________
#8. **How do you skip ssl certificate verification ?**

answer : **-K**
___________________
#9.**How do you specify a User-Agent ?**

answer : **-A**
_______________________
#10. **How do you specify a HTTP header ?**

answer : **-h**
__________________
#11. **What flag sets the URL to bruteforce ?**

answer : **-u**
________________________
#12. **Deploy the machine** 

answer : **no answer needed**
_____________
#13. **What is the name of the hidden directory ?**

    $ sudo gobuster dir -u  http://10.10.238.53 -w /usr/share/wordlists/dirb/common.txt -t 64 -x xxa  
  ![gobuster](https://res.cloudinary.com/micro0x00/image/upload/v1615286314/gobuster_x25mvh.png)

answer : **secret**
#14. **What is the name of the hidden file with the extension xxa ?**
answer : **password**
_________________
## Task 5 (Nikto)
nikto is a popular web scanning tool that allows users to find common web vulnerabilities. It is commonly used to check for common CVE's such as shellshock, and to get general information about the web server that you're enumerating.
use man command to know about it
    man nikto

________
#1. **How do you specify which host to use ?**

answer : **-h**
____________________
#2.  **What flag disables ssl?**

 answer : **-nossl**
____________
#3.  **How do you force ssl?**

 answer : **-ssl**
______
#4  **How do you specify authentication(username + pass)?**

  answer : **-id**
__________________
#5.  **How do you select which plugin to use?**
 answer : **-plugins**
___________________________________
#6. **Which plugin checks if you can enumerate apache users ?**
run `└─ $ nikto --list-plugins`
![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615288529/nako_duiykl.png)
answer : apacheusers
______________________
#7. How do you update the plugin list  ?

answer : -update
_____

#8. How do you list all possible plugins to use ?
answer : --list-plugins
______
## Task 6 (Metasploite intro)
#1.
Metasploit is one of the most popular penetration testing frameworks around. It contains a large database of almost every major CVE, which you can easily use against a machine. The aim of this section is to go through some of the major features of metasploit, and at the end there will be a machine that you will need to exploit.  
**No answer needed**
______________________
## Task 7 (Metasploite Setting up)
#### **#1**  What command allows you to search modules?

 answer : **search**

#### **#2**  How do you select a module?

answer : **use**

#### **#3**  How do you display information about a specific module?

answer : **info**

#### **#4**  How do you list options that you can set?
answer : **options**
_____
#5. **What command lets you view advanced options for a specific module ?**

answer: **advanced**
______
 #6. **How do you show options in a specific category ?**
answer : **show**
_______________________
## Task 8 (MetaSploite )
