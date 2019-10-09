# REPORTED OOPSIES

_Warning: array_map(): Argument #2 should be an array_

A very small number of plugins and themes have displayed this error after upgrading to WordPress 4.4. A fix is already in place for 4.4.1: https://core.trac.wordpress.org/ticket/34723

**This has been fixed in WordPress 4.4.1**

_Plugins and Themes Won’t Update_

An exceptionally small subset of users have reporting that after upgrading they cannot update plugins and themes. As of yet we have found no rhyme or reason for that to happen, but we are looking. If you’re having this issue, please provide as MUCH detail about your server as possible (OS, PHP version and flavor, etc). For now, you can “update” plugins and themes by deleting and installing the latest version. An official fix is in progress: https://core.trac.wordpress.org/ticket/34976

**This has been fixed in WordPress 4.4.1**

_Some posts are redirecting to old posts_

Some users are experiencing their posts redirecting to other renamed posts, this is caused by an older redirect code triggering when it shouldn’t. A bug report has been filed: https://core.trac.wordpress.org/ticket/35031

**This has been fixed in WordPress 4.4.1**

_Shortcodes Broken_

Some plugins/themes using the \[shortcode=var\] structure may be broken. As it turns out, \[shortcode=var\] only worked due to a “happy accident” and was never officially documented. Unfortunately, some plugins/theme adopted this shortcode structure when they should have used \[shortcode var\] instead. The developers are discussing a fix: https://core.trac.wordpress.org/ticket/34939

**This has been fixed in WordPress 4.4.1**