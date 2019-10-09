# LINKS GOING 404

_This INCLUDES links that break when you have category in the URL_

You may need to let WP regenerate your .htaccess.
Read http://dre.im/if-pages-return-a-404-after-wordpress-3-1-upgrade

Plugins cause this too. Especially anything screwing around with permalinks or rewrites. Note – *[Simple Tags](http://wordpress.org/extend/plugins/simple-tags/) version 1.8* has issues with 3.1. so deactivate it or turn off ‘active tags for pages’ The 2.x Beta version of the plugin is working on fixing this, but be aware it IS a beta.

FV Top Level Categories seems to have helped some people, while others have success with the [Permalink Fix & Disable Canonical Redirects Pack](http://wordpress.org/extend/plugins/permalink-fix-disable-canonical-redirects-pack/. Try installing one or the other.

Some people have found this helpful to fix redirect loop issues
http://enlightenedwebmastery.com/how-to-fix-the-redirect-loop-error-in-wordpress