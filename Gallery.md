<!-- wp:paragraph -->
<p><a href="https://tryhackme.com/room/gallery666" target="_blank" rel="noreferrer noopener">https://tryhackme.com/room/gallery666</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Run sudo nmap to find for open ports.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":922,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-21.png?w=539" alt="" class="wp-image-922"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Head to the the http site and do a searchploit on simple image.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":921,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-20.png?w=826" alt="" class="wp-image-921"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>https://www.exploit-db.com/exploits/50214 and download the exploit.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":925,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-23.png?w=1024" alt="" class="wp-image-925"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":924,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-22.png?w=820" alt="" class="wp-image-924"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":927,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-24.png?w=243" alt="" class="wp-image-927"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>https://www.revshells.com/ to generate a payload.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Start a nc listener.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":933,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-27.png?w=1024" alt="" class="wp-image-933"/><figcaption>Add in your attacking machine IP , choose bin/sh and URL encode the payload.</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Start the netcat listener</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>10.10.114.4/gallery/uploads/1649333580_TagodtjpedudxlgraadLetta.php?cmd= &lt;&lt;PASTE PAYLOAD>></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Shell is gained.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":934,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-28.png?w=588" alt="" class="wp-image-934"/><figcaption>Once connected , change to the python shell and restart the shell.</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>cat the initialize.php to find some database info</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":936,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-29.png?w=833" alt="" class="wp-image-936"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":938,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-30.png?w=654" alt="" class="wp-image-938"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Search the userdatabase and find the hash password for the admin.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Download Linpeas to the victim machine via python server form your machin.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Run linpeas</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":939,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-31.png?w=437" alt="" class="wp-image-939"/><figcaption>Found a password - b3stpassw0rdbr0xx</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Change user to mike and enter the password found on linpeas. </p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":941,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-32.png?w=294" alt="" class="wp-image-941"/><figcaption>Found the first flag</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":942,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-33.png?w=797" alt="" class="wp-image-942"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Cat the file and the we are allowed to use sudo.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to gtfobins to find a nano exploit.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":945,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-35.png?w=870" alt="" class="wp-image-945"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Run sudo nano on the rootkit.sh ^R and ^X and then type reset; sh 1>&amp;0 2>&amp;0 and root access is gained.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":944,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-34.png?w=368" alt="" class="wp-image-944"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The final flag is obtained.</p>
<!-- /wp:paragraph -->
