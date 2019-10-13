Known issues, from Nacin:

> Letting you know about two potentially nasty issues with WordPress 3.3, and
> what you should be recommending in master lists and individual forum
> threads.
> 
> ***
> 
> 1. JAVASCRIPT ISSUES. The first problem is again JSON-related. (Once
> bitten, twice WTF.)
> 
> * The symptom: Barely any JavaScript works in the admin. Meta boxes cannot
> be collapsed. Clicking the Screen Options or Help tabs don’t do anything.
> etc.
> 
> * To confirm: Go to
> http://example.com/wp-admin/load-scripts.php?load=jquery. (This page is
> accessible logged out.) If it’s blank, the bug is confirmed. Please reply
> to this thread with a link to wherever this is confirmed, as we’re curious
> as to how common this is in the wild.
> 
> * The bug: load-scripts.php may call json_encode() without us loading our
> compatibility layer. Whoops.
> 
> * The fix: It’ll be fixed in WordPress 3.3.1 (timeline still TBD), but for
> now, you can use Hotfix 0.8. Hotfix 0.8 will disable script concatenation
> and fix the problem.
> 
> * The better fix: Tell these individuals to please figure out why PHP is
> compiled to explicitly exclude JSON. I can’t even begin to explain how
> backwards that is.
> 
> ***
> 
> 2. CSS ISSUES. The second problem is related to plugin styles (or theme
> styles) bleeding into the admin.
> 
> – The symptom. Something doesn’t look right in the admin, typically on the
> dashboard, comments screen, or post/page edit screen (post-new or post.php).
> 
> – To confirm: Some CSS file from some plugin or theme is being enqueued
> when it shouldn’t be. This is visible in the source in the admin.
> 
> – The fix: It’ll be fixed in WordPress 3.3.1 (timeline still TBD), but for
> now, you can use Hotfix 0.8. Hotfix 0.8 will remove all styles accidentally
> enqueued in the admin.
> 
> – The better fix: One of their plugins is guilty of using the wrong hook.
> There’s a bit of nuance here, but I’ve posted a summary at
> http://wpdevel.wordpress.com/2011/12/12/use-wp_enqueue_scripts-not-wp_print_styles-to-enqueue-scripts-and-styles-for-the-frontend/
> .
> 
> ***
> 
> More about Hotfix: Hotfix is a plugin maintained by lead developer Mark
> Jaquith and some other core developers including myself. Users should leave
> the plugin active (or at least installed) and always updated, in the case
> of quick patches for future releases. The current version is 0.7. Mark will
> release 0.8 in the morning. The development version is 0.8:
> http://wordpress.org/extend/plugins/hotfix/download/.
> 
> ***
> 
> The full list of known, reported, and confirmed issues is at
> http://core.trac.wordpress.org/report/4.
> 
> Cheers,
> Nacin

ETA (Dec 16th) – If you use Multisite and DO NOT have a DB prefix (i.e. wp_) on your database, there may be some problems. Strictly speaking, that’s not supported as it does silly things with your settings if you later try to turn on multisite, but that being said, it looks like the core devs may have to reinstate things for 3.3.1. Keep tabs on http://core.trac.wordpress.org/ticket/19566 for more gory details. Oh and in the future, **please** use db prefixes. Every app, from WordPress to those professional ones people pay millions for suggests you use them.