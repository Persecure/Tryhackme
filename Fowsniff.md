<!-- wp:paragraph -->
<p>Link to the ctf : <a href="https://tryhackme.com/room/ctf" target="_blank" rel="noreferrer noopener">https://tryhackme.com/room/ctf</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>Using nmap, scan this machine. What ports are open?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Start with a nmap scan to find for open ports.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>4 ports are open</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><mark style="background-color:rgba(0, 0, 0, 0);" class="has-inline-color has-primary-color"><strong>Using Google, can you find any public information about them?</strong></mark></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Search in google for FowSniff and a Twitter account is found.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":883,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-2.png?w=634" alt="" class="wp-image-883"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Scroll the posts and this is found. </p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":885,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-3.png?w=594" alt="" class="wp-image-885"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>Can you decode these md5 hashes? You can even use sites like hashkiller to decode them.</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to  https://pastebin.com/NrAqVeeX to find users and md5 hashes.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":886,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-4.png?w=944" alt="" class="wp-image-886"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Head to https://hashes.com/en/decrypt/hash to decrypt the md5 hashes.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":880,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image.png?w=1024" alt="" class="wp-image-880"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Save the users in one file.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":889,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-6.png?w=648" alt="" class="wp-image-889"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>And the cracked passwords in anther file.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":891,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-7.png?w=646" alt="" class="wp-image-891"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>Using the usernames and passwords you captured, can you use metasploit to brute force the pop3 login?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Start up msfconsole and search for pop3 and use the third exploit.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":888,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-5.png?w=828" alt="" class="wp-image-888"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Set the RHOSTS , USERS FILE and PASSWORD FILE and run the exploit. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>What was seina's password to the email service?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":896,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-8.png?w=831" alt="" class="wp-image-896"/><figcaption>scoobydoo2</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>Can you connect to the pop3 service with her credentials? What email information can you gather?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>start a netcat listener to the box with port 110.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":898,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-9.png?w=565" alt="" class="wp-image-898"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>Looking through her emails, what was a temporary password set for her?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":899,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-10.png?w=669" alt="" class="wp-image-899"/><figcaption>S1ck3nBluff+secureshell</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>In the email, who send it? Using the password from the previous question and the senders username, connect to the machine using SSH</strong>.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":902,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-11.png?w=518" alt="" class="wp-image-902"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":907,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-13.png?w=804" alt="" class="wp-image-907"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size"><strong>Once connected, what groups does this user belong to? Are there any interesting files that can be run by that group?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":909,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-14.png?w=286" alt="" class="wp-image-909"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>nano cube.sh and paste the python reverse shell script. Change the IP address to your attacking machine IP</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":912,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-16.png?w=822" alt="" class="wp-image-912"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Exit the ssh , start a netcat listener and login to the ssh user again</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":913,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-17.png?w=516" alt="" class="wp-image-913"/><figcaption>Root shell gained</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":914,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-18.png?w=320" alt="" class="wp-image-914"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Cat the flag.txt to get the final flag.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":916,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-19.png?w=837" alt="" class="wp-image-916"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->
