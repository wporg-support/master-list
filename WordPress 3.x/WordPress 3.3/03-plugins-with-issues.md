# PLUGINS WITH ISSUES

In all cases, make sure you’re using the latest version of the plugin. Many plugins have updated and will now work with 3.3, but upgrade the plugins first before reporting an issue. For people who reported a plugin to me before, I tested them all out on a clean install of WP with only that plugin installed. If it worked, I removed it from this list. Plugin conflicts aren’t the same as plugins not working on 3.3

* _Plugin CSS bleeding into the admin_

> Cause: The plugin is hooking into the wp_print_styles hook.
> 
> Fix: Hook into the wp_enqueue_scripts hook (for scripts or styles).
> 
> More: http://wpdevel.wordpress.com/2011/12/12/use-wp_enqueue_scripts-not-wp_print_styles-to-enqueue-scripts-and-styles-for-the-frontend/
> 
> Gory details: http://core.trac.wordpress.org/ticket/19510

* Reports on twitter that the _Postie_ plugin breaks 3.3 admin.

* _Popup Domination_ (a plugin NOT available on the WordPress repository) is breaking 3.3. There is an update, but as this is a premium (i.e. you buy it) plugin, you’re not going to get a lot of support here.

* _IntenseDebate_ is showing a miss-match of comments pending.

* _Count Per Day_ breaks the Media Uploader.

* _Advanced Access Manager_ causes a white screen of death.

* _TubePress_ interferes with drag’n’drop in the Admin area.

* _White Label CMS_ breaks image insertion.

* _All In One SEO_ reported to lose all custom menu label tags.
http://wordpress.org/support/topic/menu-label-issue-in-wp33-upgrade

* _Improved Page Permalinks_ reported to cause newly published Pages to produce 404s.

* _Ad blocker_ plugins may conflict with the visual editor.

* _Viperbar_ may become de-enabled and lose all settings.
http://wordpress.org/support/topic/plugin-viperbar-plug-in-deactivateds-itself-and-loses-data-on-upgrade-to-wp-33

* _Google XML Sitemaps_ 4.0Beta7 has blank line
http://wordpress.org/support/topic/plugin-google-xml-sitemaps-beta-7-broken-on-wordpress-33?replies=1

* _WordPress MU Domain Mapping_ doesn’t let you change settings. The dev version fixes this.

* _WordPress MU Sitewide Tags Plugin_ also has issues, please try the dev version of that plugin too.