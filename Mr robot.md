<!-- wp:paragraph -->
<p>Run a nmap scan to find for open ports.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":967,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-44.png?w=603" alt="" class="wp-image-967"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Run dirb to scan for website directories.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":964,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-43.png?w=655" alt="" class="wp-image-964"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Download the fsocity.dic file (contains a list for bruteforcing) and head to key-1-of-3.txt to find the first flag.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":955,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-39.png?w=536" alt="" class="wp-image-955"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Capture the request in Burpsuite.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":953,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-38.png?w=951" alt="" class="wp-image-953"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>"log=admin&amp;pwd=test" this parameter is needed for the bruteforce attack.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Forward the capture and an ERROR message is found.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":957,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-40.png?w=476" alt="" class="wp-image-957"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Star up hydra with the following command:</p>
<!-- /wp:paragraph -->

<!-- wp:code -->
<pre class="wp-block-code"><code><code>hydra -L /home/kali/Downloads/fsocity.dic -p test 10.10.108.57 http-post-form "/wp-login.php:log=^USER^&amp;pwd=^PASS^:Invalid username" -t 30</code>
</code></pre>
<!-- /wp:code -->

<!-- wp:paragraph -->
<p>Use the userlist from the dictionary found in the beginning. The password is just a test. The http-post-form inputs are taken from the burpsuite capture and add "Invalid username" to filter out the user list.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":960,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-41.png?w=1024" alt="" class="wp-image-960"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>User Elliot is found.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":962,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-42.png?w=437" alt="" class="wp-image-962"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Now the user is found let's bruteforce the password with the dictionary list with WPSCAN.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":970,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-45.png?w=964" alt="" class="wp-image-970"/><figcaption>password found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Head to the editor and insert a php reverse shell in one of the pages.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":971,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-46.png?w=1024" alt="" class="wp-image-971"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Start up the listener an access is gained.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":972,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-47.png?w=861" alt="" class="wp-image-972"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":974,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-49.png?w=364" alt="" class="wp-image-974"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Use a password hash cracker to get the password</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":973,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-48.png?w=1024" alt="" class="wp-image-973"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Use python -c 'import pty; pty.spawn("/bin/bash")' to launch a shell and switch user to robot.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":976,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-50.png?w=418" alt="" class="wp-image-976"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":978,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-51.png?w=312" alt="" class="wp-image-978"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The second flag is gained.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":979,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-52.png?w=516" alt="" class="wp-image-979"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Gain root access by exploiting nmap</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":980,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-53.png?w=443" alt="" class="wp-image-980"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":982,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-54.png?w=826" alt="" class="wp-image-982"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":983,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-55.png?w=605" alt="" class="wp-image-983"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":985,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/04/image-56.png?w=757" alt="" class="wp-image-985"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The final flag is gained. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->
