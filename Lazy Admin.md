# LazyAdmin-CTF
https://tryhackme.com/room/lazyadmin

**use nmap -sS -A -p- IP address to scan for open ports**

PORT   STATE SERVICE VERSION

22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)

80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))

**Use gobuster on web server**

found the following

/content/
/content/as/

webserver is under SweetRice 

Search for exploit online - **SweetRice 1.5.1 - Backup Disclosure** 

You can access to all mysql backup and download them from this directory.

http ://localhost/inc/mysql_backup

There is a mysql file that contains the user and password in hash 

**Use an online rainbow table to crack the password : Password123**

Head to /content/as and login with the new found details

Head to the ads section and you are able insert scripts

**Use a php rever shell script from https: //github.com/pentestmonkey/php-reverse-shell**

start up netcat 

head to the uploads directory http://(ip)/content/inc/ads/ and click the php script

netcat has started and gian user access 

cat user.txt to get the first flag

sudo -l and some details are provided

(ALL) NOPASSWD: /usr/bin/perl /home/itguy/backup.pl

cat /etc/copy.sh

It is another revershell script , use echo to edit the file with your ip and port

start up another netcat

execute copy.sh 

root access is gained

cat root.txt to get the final flag



## What is the user flag?

:pirate_flag:THM{63e5bce9271952aad1113b6f1ac28a07}

## What is the root flag?

:pirate_flag:THM{6637f41d0177b6f37cb20d775124699f}





