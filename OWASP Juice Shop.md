OWASP Juice Shop

Task 3

Question #1: Log into the administrator account!

Head to the login page.

Startup Burpsuite and intercept the login page with a random user and password.


Change the email details with ‘ or 1=1– and forward it to the server


Access gained and the first flag found.


Question #2: Log into the Bender account!

Repeat the previous steps but with the bender email account.


Add ‘– to the end of the email.


Access gained and the second flag found.


Task 4

Question #1: Bruteforce the Administrator account’s password!

Intercept the login page with the admin account and send it to intruder.


Change the password to just $$


Download a password list from best1050.txt from Seclists. and load it into the payload.


Run the attack and set the status arrow to up, If the status is 200 the password is gained.


The password is admin123

Flag is found
Question #2: Reset Jim’s password!


Resetting Jim’s password
Do a google for Jim star trek and head to the wiki page.


Samuel is the middle name of the only sibling
Insert the new password and the flag is found.


Task 5

Question #1: Access the Confidential Document!

Head to the site’s About us page and there will be a link.


The link leads to a ftp directory.



FTP server is found
Download the acquisitions.md and head to the site to find a flag.


Question #2: Log into MC SafeSearch’s account!



Flag is found
Question #3: Download the Backup file!

Download the package.json.bak file and the following error will be shown.


.json files are allowed and need to be bypass




Flag is found
Task 6

Question #1: Access the administration page!

Open debugger under web developer tools and refresh the page. main-es2015.js will be shown.



Search for the administration path
Login with the admin account and head to #/administration.


A flag is found
Question #2: View another user’s shopping basket!

Head to the admin’s basket and capture it via burpsuite.

Forward the request till you reach the basket capture.


Change the number to 2 to get a flag.


Question #3: Remove all 5-star reviews!

Head to the administration page.


Remove the star rating by clicking on the bin.




Flag is found
Task 7

Question #1: Perform a DOM XSS!

Input the following DOM XSS script in the search bar :

1
<iframe src="javascript:alert(`xss`)"> 

Flag is found
Question #2: Perform a persistent XSS!

Head to the Last Login IP page under Account , Privacy & Security


Start up Burpsuite to intercept the request.

Logout of the account and head to Burpsuite.



Flag is found

Question #3: Perform a reflected XSS!

Login to the admin account and head over to the order history page.


Click on the Truck icon and in the URL you will see the following.


Replace with the iframe XSS script.


Flag is found
Task 8

Access the /#/score-board/ page


Final flag is found
