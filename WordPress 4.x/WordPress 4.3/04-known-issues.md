# KNOWN ISSUES

_Chrome 45 messed up the admin menus_

This isn’t a WordPress 4.3 issue but I’m including it here because some users will see this as a 4.3 issue.

Chrome 45 has a rendering bug. There is a ticket open on Chrome’s bug tracker about this issue.

*'Chrome released a fix for this on September 15th**. Update your version of Chrome to the latest Stable and it will be corrected.

_Plugins_

- [RevSlider](http://codecanyon.net/item/slider-revolution-responsive-wordpress-plugin/2751380) (a premium plugin) has been reported to not run on WP 4.3. Please update to **5.0.4.1** (released Aug 18th) to correct.
- [WP Ban](https://wordpress.org/plugins/wp-ban/) needs to be upgraded to **1.66**
- [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/) has been reported to have issues with the RSS feeds in WordPress 4.3. The current workaround is to disable RSS Feed Caching on the Page Cache settings page, and then to Purge all caches.
- [OptimizePress](https://www.optimizepress.com/) sends registration emails with the password set to ‘both’. Please [disable that setting](https://optimizepress.zendesk.com/hc/en-us/articles/207299298) in OptimizePress

_**WP_Widget error**_

If you are getting this message on your WordPress installation:

```
The called constructor method for WP_Widget is deprecated since version 4.3.0! Use __construct()
```

Then your theme or plugin need to be updated. As a temporary work around look for `define( 'WP_DEBUG', true );` in your `wp-config.php` file and set that to `false`.

If you look in the wp-config.php file and find that WP_DEBUG is already set to false, then please contact your hosting service, and ask them for the proper way for you to disable the PHP `display_errors` setting on your website. The `display_errors` setting is a developer mode setting, and it should never be enabled for a live website.

That only causes the warning to not be displayed, [the theme or plugin should be updated](https://make.wordpress.org/core/2015/07/02/deprecating-php4-style-constructors-in-wordpress-4-3/).

_**I use SSH2 for updating, and I cannot update plugins or themes anymore**_

This is a known issue in 4.3 and there is a fix available which will be in 4.3.1. You can read more about the issue [at this link](https://core.trac.wordpress.org/ticket/33480). If you wish to apply the patch yourself in the meantime, you can find it here: https://core.trac.wordpress.org/changeset/33688

_**Extreme slowdown, heavy CPU load, site being inaccessible after a while**_

WordPress 4.3 accidentally contained a minor bug relating to term-splitting, which in some rare cases, can cause a large number of wp-cron jobs to build up which will never actually complete. This issue is already fixed, and the issue will be solved by WordPress 4.3.1.

However, until that is ready, you can fix the problem yourself by following these instructions. Be sure to follow the instructions carefully and in the order that they are given:
https://wordpress.org/support/topic/high-cpu-load-after-update-to-v43?replies=17#post-7330770