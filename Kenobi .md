<!-- wp:paragraph -->
<p>Walkthrough on exploiting a Linux machine. Enumerate Samba for shares, manipulate a vulnerable version of proftpd and escalate your privileges with path variable manipulation.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a rel="noreferrer noopener" href="https://tryhackme.com/room/kenobi" data-type="URL" data-id="https://tryhackme.com/room/kenobi" target="_blank">https://tryhackme.com/room/kenobi</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Task 1</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Scan the machine with nmap, how many ports are open? </strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":679,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-18.png?w=565" alt="" class="wp-image-679"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>7</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Task 2</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse &lt;IP></code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p><strong>Using the nmap command above, how many shares have been found?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":681,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-19.png?w=677" alt="" class="wp-image-681"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>3</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Once you're connected, list the files on the share. What is the file can you see?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":683,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-20.png?w=782" alt="" class="wp-image-683"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>log.txt</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You can recursively download the SMB share too. Submit the username and password as nothing.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":685,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-21.png?w=563" alt="" class="wp-image-685"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong>What port is FTP running on?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>cat the newly downloaded log.txt file to find the FTP port number.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":688,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-22.png?w=315" alt="" class="wp-image-688"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>21</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>What mount can we see?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount &lt;IP></code></pre>
<!-- /wp:code -->

<!-- wp:image {"id":690,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-23.png?w=599" alt="" class="wp-image-690"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>/var</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Task 3</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Lets get the version of ProFtpd. Use netcat to connect to the machine on the FTP port.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>What is the version?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":692,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-24.png?w=596" alt="" class="wp-image-692"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>1.3.5</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>How many </strong>exploits are there for the ProFTPd running?</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":694,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-25.png?w=870" alt="" class="wp-image-694"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>4</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Copy Kenobi's private key using SITE CPFR and SITE CPTO commands.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":696,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-26.png?w=651" alt="" class="wp-image-696"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Mount the /var/tmp directory to our machine</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":698,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-27.png?w=571" alt="" class="wp-image-698"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Copy the rsa file to your directory and chmod the file.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":700,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-28.png?w=435" alt="" class="wp-image-700"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":701,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-29.png?w=224" alt="" class="wp-image-701"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>SSH into the kenobi server.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":703,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-30.png?w=665" alt="" class="wp-image-703"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong>What is Kenobi's user flag (/home/kenobi/user.txt)?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":704,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-31.png?w=380" alt="" class="wp-image-704"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>d0b0f3f53b6caa532a83915e19224899</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Task 4</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":705,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-32.png?w=479" alt="" class="wp-image-705"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong>What file looks particularly out of the ordinary?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><em>/usr/bin/menu</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Run the following commands.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":707,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-33.png?w=658" alt="" class="wp-image-707"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong>Run the binary, how many options appear?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":709,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-34.png?w=872" alt="" class="wp-image-709"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>3</em></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>What is the root flag (/root/root.txt)?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":710,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-35.png?w=323" alt="" class="wp-image-710"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><em>177b3cd8562289f37382721c28381f02</em></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":714,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/03/image-36.png?w=359" alt="" class="wp-image-714"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->
