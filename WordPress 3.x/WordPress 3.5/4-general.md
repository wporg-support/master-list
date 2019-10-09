# General

**Error message:** `Warning: Missing argument 2 for wpdb::prepare(), called in ...` (happens in themes and plugins)

**Fix**: Your site is fine, but you may wish to turn off PHP’s display errors setting. Contact your theme or plugin dev and point them to http://make.wordpress.org/core/2012/12/12/php-warning-missing-argument-2-for-wpdb-prepare/ so they can fix the underlying issue.

**Error message**: `Download failed. Destination directory for file streaming does not exist or is not writable.`

**Fix**: When WordPress downloads any sort of file, then it has to be able to write that file somewhere. To do this, it uses the “temp” directory. If WP detects that it cannot write files to this temp directory, then you get the error message you are now getting. WP tries to find a valid temp directory, but sometimes servers are configured poorly.

WordPress 3.5 changed the temp directory order to prefer the system’s pre-defined temp directory instead of attempting to write into wp-content. On some badly configured hosting systems, this temp directory may be defined, but not actually writable. This causes the error message.

You can work around this by specifying a temp directory on your server with a place that you know WordPress is allowed to write files to. You can do this by adding this line of code into the wp-config.php file.
`define( 'WP_TEMP_DIR' , ABSPATH . 'wp-content/' );`

That will tell WP where to write the temporary files.

_Themes_

- **Twenty Twelve**

On Appearance > Themes, if you see “twentytwelve – Stylesheet is missing” under “Broken Themes”, then you have this problem. (Multisite: You can find broken themes on Network Admin > Themes.) This only affects individuals who updated to WordPress 3.5 in the first hour of its release, and who didn’t already have Twenty Twelve installed.

Fix: Install the Hotfix plugin – http://wordpress.org/extend/plugins/hotfix/ – then update Twenty Twelve.

Or, you can fix this manually: connect to your server via FTP, then remove the empty `wp-content/themes/twentytwelve` directory. Then, go to Appearance > Themes > Install Themes and search for and install Twenty Twelve. (Or find it on the Featured tab.)

- **Curation Traffic**

http://curationtraffic.com/ causes a missing argument with wpdb::prepare. See http://wordpress.org/support/topic/missing-argument-1?replies=2 for more information.

- **SmallBiz theme**

http://www.expand2web.com/smallbiz-theme/

Multiple reports of the theme interfering with Jetpack stats and the movement, opening or editing of any widgets.
eg. http://wordpress.org/support/topic/have-trouble-in-35-with-jetpack-widgets

- **Minimatica Theme**

http://wordpress.org/extend/themes/minimatica

Confirmed conflicts with new media uploader. Unable to view media library or set featured image.

**fix**

Replace functions.php with this version that comments out erroneous ext2type filter and improper registering and enqueueing of javascript.

_Plugins_

- **WordPress Polls version 33.7** – http://wordpress.org/extend/plugins/cardoza-wordpress-poll

Upgrade to the latest version.

- **Role Scoper** – http://wordpress.org/extend/plugins/role-scoper/

Issues with Custom Post Types. Author has been emailed.

- **Select Featured Posts** – http://wordpress.org/extend/plugins/select-featured-posts/

Displays wpdb::prepare() error – Author has been emailed.

- **BulletProof Security** – http://wordpress.org/extend/plugins/bulletproof-security/

Update to the latest version (.47.7) to fix issues with javascript functionality in WordPress not working correctly.

Note: You can still have this problem if you have *ever* used the BulletProof Security in the past, even if you have removed it. If you are experiencing problems with menus and widgets and the editor and similar not working, and you have ever used BulletProof Security, even if you’re not using it anymore, then look for an .htaccess file in the /wp-admin directory, and delete it if it is there.

- **Widget Logic Visual** – http://www.totalbounty.com/freebies/widget-logic-visual/

JS errors. Only fix is to deactivate and delete.

- **Cart66 Lite** – http://wordpress.org/extend/plugins/cart66-lite/

Add Media and Edit Permalink buttons on the page and post edit screens to not work