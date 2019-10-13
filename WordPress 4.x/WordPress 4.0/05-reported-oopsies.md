# REPORTED OOPSIES

_Themes_

\* Thesis 1.8.5 has assorted issues involving comments disappearing and reports of 500 server errors. [Thesis has a fix for this.](http://diythemes.com/forums/showthread.php?100176-Thesis-1.8.5-WordPress-4.0-Comments-Not-Showing)

Reported fix instructions:

> NOTE: You must be using version 1.8.5 before deploying this fix; if you’re still using an outdated 1.x version, then you must update Thesis first.
> 
> 1. Using FTP, navigate to the /wp-content/themes/thesis_185/lib/classes/ folder on your server.
> 
> 2. Edit the comments.php file in the classes folder at line 187, instead of
> 
> ```
> $wp_query->comments_by_type = &separate_comments($wp_query->comments);
> $_comments = $wp_query->comments_by_type['comment'];
> ```
> 
> you now write
> 
> ```
> $wp_query->comments_by_type = separate_comments($wp_query->comments);
> $_comments = &$wp_query->comments_by_type['comment'];
> ```
> 
> The only change is moving the “&” to the $_comments-variable really but that seems to cause the 500 internal server errors.
> 
> Once you’ve followed these steps, check to see if your comments are now being displayed correctly.

_Plugins_

\* [Comprehensive Google Map Plugin](https://wordpress.org/plugins/comprehensive-google-map-plugin/) – Breaks Media buttons
\* [Genesis Title Toggle](https://wordpress.org/plugins/genesis-title-toggle/) – Breaks Media buttons _FIXED IN LATEST VERSION_
\* [Markdown Quicktags](https://wordpress.org/plugins/markdown-quicktags/) – Breaks media buttons
\* [All in One SEO pack](https://wordpress.org/plugins/all-in-one-seo-pack/) – Breaks media buttons, but an update to fix this is available. Update the plugin.
\* [WordPress IPSConnect](http://community.invisionpower.com/files/file/6089-wordpress-ipsconnect/) – Causes every link to have an “Are You Sure?” screen, due to nonce changes in WordPress 4.0. Any plugin that bridges users between different apps like this is likely to have the same problem until it has been updated.
\* [WPML Media](http://wpml.org/) – Uploading any media leads to an error and a large amount of identically named (and corrupted) files. Upgrade to resolve.

_Hosting_

\* GoDaddy – Due to a server configuration, some updated WordPress files may have been prevented from being copied over, resulting in a white-screen-of-death or an error message similar to the following:

```
Warning: require_once(/.../wp-admin/includes/image.php)
[function.require-once]: failed to open stream: No such file or directory
in /.../wp-admin/includes/admin.php on line 28
Fatal error: require_once() [function.require]: Failed opening required
'/.../wp-admin/includes/image.php'
(include_path='.:/usr/local/php5_3/lib/php') in
/.../wp-admin/includes/admin.php on line 28
```

If this happens, try [downloading WordPress](http://wordpress.org/download/) again and delete then replace your copies of everything except the `wp-config.php` file and the `/wp-content/` directory with fresh copies from the download. Performing a [manual update](http://codex.wordpress.org/Updating_WordPress#Manual_Update) will fix the problem of missing files.