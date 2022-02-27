<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Task 3</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #1: Log into the administrator account!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to the login page.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Startup Burpsuite and intercept the login page with a random user and password.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":274,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-14.png?w=875" alt="" class="wp-image-274"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Change the email details with  ' or 1=1-- and forward it to the server</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":276,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-15.png?w=873" alt="" class="wp-image-276"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Access gained and the first flag found.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":278,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-16.png?w=779" alt="" class="wp-image-278"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #2: Log into the Bender account!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Repeat the previous steps but with the bender email account.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":281,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-17.png?w=875" alt="" class="wp-image-281"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Add   '-- to the end of the email.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":283,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-18.png?w=871" alt="" class="wp-image-283"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Access gained and the second flag found.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":285,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-19.png?w=681" alt="" class="wp-image-285"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Task 4</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #1: Bruteforce the Administrator account's password!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Intercept the login page with the admin account and send it to intruder.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":287,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-20.png?w=795" alt="" class="wp-image-287"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Change the password to just $$</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":289,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-21.png?w=750" alt="" class="wp-image-289"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Download a password list from best1050.txt from Seclists. and load it into the payload.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":292,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-22.png?w=879" alt="" class="wp-image-292"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Run the attack and set the status arrow to up, If the status is 200 the password is gained.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":324,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-38.png?w=531" alt="" class="wp-image-324"/><figcaption>The password is admin123</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":325,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-39.png?w=1024" alt="" class="wp-image-325"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #2: Reset Jim's password!</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":327,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-40.png?w=501" alt="" class="wp-image-327"/><figcaption>Resetting Jim's password</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Do a google for Jim star trek and head to the wiki page.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":329,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-41.png?w=265" alt="" class="wp-image-329"/><figcaption>Samuel is the middle name of the only sibling</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Insert the new password and the flag is found.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":331,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-42.png?w=669" alt="" class="wp-image-331"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Task 5</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #1: Access the Confidential Document!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to the site's About us page and there will be a link.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":333,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-43.png?w=1024" alt="" class="wp-image-333"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The link leads to a ftp directory.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":335,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-44.png?w=200" alt="" class="wp-image-335"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":336,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-45.png?w=1024" alt="" class="wp-image-336"/><figcaption>FTP server is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Download the acquisitions.md and head to the site to find a flag.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":338,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-46.png?w=745" alt="" class="wp-image-338"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #2: Log into MC SafeSearch's account!</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":340,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-47.png?w=1024" alt="" class="wp-image-340"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":342,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-48.png?w=739" alt="" class="wp-image-342"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #3: Download the Backup file!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Download the package.json.bak file and the following error will be shown.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":344,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-49.png?w=1024" alt="" class="wp-image-344"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>.json files are allowed and need to be bypass</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":346,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-50.png?w=920" alt="" class="wp-image-346"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":348,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-51.png?w=1024" alt="" class="wp-image-348"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":350,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-52.png?w=894" alt="" class="wp-image-350"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Task 6</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #1: Access the administration page!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Open debugger under web developer tools and refresh the page. main-es2015.js will be shown.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":352,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-53.png?w=515" alt="" class="wp-image-352"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":354,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-54.png?w=904" alt="" class="wp-image-354"/><figcaption>Search for the administration path </figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Login with the admin account and head to #/administration.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":356,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-55.png?w=791" alt="" class="wp-image-356"/><figcaption>A flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #2: View another user's shopping basket!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to the admin's basket and capture it via burpsuite.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Forward the request till you reach the basket capture.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":358,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-56.png?w=863" alt="" class="wp-image-358"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Change the number to 2 to  get a flag.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":360,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-57.png?w=705" alt="" class="wp-image-360"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #3: Remove all 5-star reviews!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to the administration page.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":394,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-65.png?w=312" alt="" class="wp-image-394"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Remove the star rating by clicking on the bin.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":396,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-66.png?w=1024" alt="" class="wp-image-396"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":398,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-67.png?w=1024" alt="" class="wp-image-398"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":399,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-68.png?w=779" alt="" class="wp-image-399"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Task 7</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #1: Perform a DOM XSS!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Input the following DOM XSS script in the search bar :</p>
<!-- /wp:paragraph -->

<!-- wp:syntaxhighlighter/code {"language":"jscript"} -->
<pre class="wp-block-syntaxhighlighter-code">&lt;iframe src="javascript:alert(`xss`)"> </pre>
<!-- /wp:syntaxhighlighter/code -->

<!-- wp:image {"id":402,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-69.png?w=1024" alt="" class="wp-image-402"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Question #2: Perform a persistent XSS!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Head to the Last Login IP page under Account , Privacy &amp; Security</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":404,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-70.png?w=1024" alt="" class="wp-image-404"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Start up Burpsuite to intercept the request.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Logout of the account and head to Burpsuite.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":406,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-71.png?w=1024" alt="" class="wp-image-406"/></figure>
<!-- /wp:image -->

<!-- wp:image {"id":407,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-72.png?w=1024" alt="" class="wp-image-407"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":409,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-73.png?w=1024" alt="" class="wp-image-409"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Question #3: Perform a reflected XSS!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Login to the admin account and head over to the order history page.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":411,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-74.png?w=1024" alt="" class="wp-image-411"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Click on the Truck icon and in the URL you will see the following.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":413,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-75.png?w=496" alt="" class="wp-image-413"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Replace with the iframe XSS script.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":415,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-76.png?w=1024" alt="" class="wp-image-415"/><figcaption>Flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:paragraph {"fontSize":"large"} -->
<p class="has-large-font-size">Task 8</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph {"fontSize":"medium"} -->
<p class="has-medium-font-size">Access the /#/score-board/ page</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":417,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-77.png?w=908" alt="" class="wp-image-417"/><figcaption>Final flag is found</figcaption></figure>
<!-- /wp:image -->

<!-- wp:image {"id":419,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://persecure.files.wordpress.com/2022/02/image-78.png?w=520" alt="" class="wp-image-419"/></figure>
<!-- /wp:image -->
