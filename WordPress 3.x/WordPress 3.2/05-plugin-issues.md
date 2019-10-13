# PLUGIN ISSUES

**BuddyPress**
http://wordpress.org/extend/plugins/buddypress/

BuddyPress 1.2.8 has a couple of small issues with WordPress 3.2, mainly with javascript in the BP-Default theme. New version released on July 5th resolves this.

**Facebook Comments for WordPress**
http://wordpress.org/extend/plugins/facebook-comments-for-wordpress/

Causes “Plugin could not be activated because it triggered a fatal error.” on activation. Also seems to cause issues if left on when upgrading.

**WP-Insert**
http://wordpress.org/extend/plugins/wp-insert/

Causes all the side bars in the admin dashboard to vanish. New version released on July 5th resolves this.

**Tweet This**
http://wordpress.org/extend/plugins/tweet-this/

Causes a fatal error due to a dependency on the class-json.php file. See Missing class-json.php above.

To fix the plugin, edit the tweet-this.php file. On line 137, you’ll find this code:

```
/**
 * JSON functions.
 * @package tweet-this
 * @since 1.7
 */
if(!class_exists('Services_JSON')) {
	if(version_compare($GLOBALS['wp_version'], '2.9', '<'))
		require_once(TT_JSON);
	else require_once(TT_WP_JSON);}
if(!function_exists('json_encode')) {
	function json_encode($data) {
		$json = new Services_JSON();
		return($json->encode($data));}}
if(!function_exists('json_decode')) {
	function json_decode($data) {
		$json = new Services_JSON(SERVICES_JSON_LOOSE_TYPE);
		return($json->decode($data));}}
```

Simply remove that section of code entirely and save. Then all is well. That code is no longer necessary with PHP 5, which has the json functions built in.

**Tweet Blender**

Throws JSON errors. The plug-in developer has released a 3.2-compatible version (3.3.10) which fixes the issue: http://bit.ly/pvNPuA

**Headspace2 SEO**
http://wordpress.org/extend/plugins/headspace2/

Reported to cause menu toggling issues in the Dashboard.

**Block-Spam-By-Math-Reloaded**
http://wordpress.org/extend/plugins/block-spam-by-math-reloaded/

Reported to interfere with the site administrator’s ability to reply to comments.

**List Rank Dashboard Widget**
http://wordpress.org/extend/plugins/list-rank-dashboard-widget/
```
Fatal error: Call to undefined function register_setting() in /home/content/k/i/w/kiwivic/html/wp-content/plugins/list-rank-dashboard-widget/wp-list-rank-class.php on line 156.
```

**JJ NextGen JQuery Slider**
http://wordpress.org/extend/plugins/jj-nextgen-jquery-slider/

Slider no longer works: images only change on screen refresh, no nav displayed.

**FeedWordPress** 
http://wordpress.org/extend/plugins/feedwordpress/

Causes
```
Fatal error: Call to undefined method WP_SimplePie_File::wp_simplepie_file() in /*/wp-content/plugins/feedwordpress/feedwordpress.php on line 1841
```

Fix from ricardofpraimundo:

> Search line 1841
> `WP_SimplePie_File::WP_SimplePie_File($url, $timeout, $redirects, $headers, $useragent, $force_fsockopen);`
> 
> replace with
> `parent::__construct($url, $timeout, $redirects, $headers, $useragent, $force_fsockopen);`

**Theme My Login**
http://wordpress.org/extend/plugins/theme-my-login/

Locks users out of their sites.

**Grooveshark Plugin for WordPress**
Makes it so you can’t upload images.

**Digi Traffic Multiplier**
Yet another “left hand menu is missing” problem. The latest version of the plugin should resolve this.

**jQuery Colorbox**
http://wordpress.org/extend/plugins/jquery-colorbox/

You need to upgrade to the 4.1 version

**jQuery.easein**
Seems to conflict with the new jQuery in WP. No fix at this time.

**Disqus Comment System**
http://wordpress.org/extend/plugins/disqus-comment-system/

Breaks the jquery interfaces so you can’t add images to posts, drag widgets, etc.