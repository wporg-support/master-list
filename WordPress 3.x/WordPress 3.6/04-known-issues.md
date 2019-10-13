# KNOWN ISSUES

_jQuery_

Plugins and themes which use their own jQuery without properly compensating for WP’s will break. Again. jQuery was upgraded in 3.6, so even though this should be much less of a problem, please take note. (Plugin and Theme Devs – Please stop using your own version of jquery!)

See https://core.trac.wordpress.org/ticket/22896 for more details.

Also many sites are producing a 404 error looking for /wp-includes/js/jquery/jquery-1.10.2.min.map. This will be fixed in 3.6.1

http://core.trac.wordpress.org/ticket/24994
http://core.trac.wordpress.org/ticket/24879

_jQuery BlockUI alert error_

Plugins and themes that happen to be using jQuery.BlockUI may have an interesting error where they get a popup saying that they need to use jQuery later than v 1.2.3 even though WordPress is using 1.10.1

This is caused by math not acting the way humans assume it will. In older versions of the jQuery.BlockUI code used by plugins there is a little ‘buglet’ – the code tests for versions BUT drops the trailing ‘0’, so instead of asking is 1.10 greater than 1.2, it tests if 1.1 is greater than 1.2, and so it fails.

To fix this, you need to update the theme/plugin having the issue. From [ChipsOnFire](http://wordpress.org/support/topic/wordpress-36-and-jqueryblockui-version-problem-solution?replies=6#post-4486355), here’s his solution:

> My plugin used a file called wf-an-jqery-plugins.js. Inside that file was a chunk of jQery.BlockUI code that said it was v2.39.
> 
> I went to the following link for the latest jQuery.BlockUI code (v2.64) and then just replaced the v2.39 code in that plugin file with the code from this link. Hey presto, it all works again: http://malsup.github.io/jquery.blockUI.js

This is not something WP did wrong, it’s just how computers sometimes decide to order numbers in non-sensible ways. The reason this wasn’t caught in testing was apparently none of the beta testers were using old BlockUI code.

_Audio/Video Plugins_

Since WordPress now auto-emebeds audio and video (and uses the \[audio\] and \[video\] shorttags), any plugin or theme that adds those in may conflict.