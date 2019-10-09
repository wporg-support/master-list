# ADMIN BAR

You can turn this off for yourself in your profile.

If it’s throwing your theme out of whack, make sure you have a call to `wp_footer()` in your theme’s footer. The next cause for that is your theme’s css having a conflict. If it’s your avatar size, again, that’s CSS. Check out this link for more info: http://voodoopress.com/2011/02/wordpress-3-1-admin-bar-upgrade-issues/

Wanna turn the admin menu ON for EVERYONE? Use the [Always Show Admin Bar Function](http://blog.ftwr.co.uk/archives/2011/01/05/always-show-admin-bar/)

Like the bar but not the search? [Hide Admin Bar Search Plugin](http://wordpress.org/extend/plugins/hide-admin-bar-search/) is there.

Want to minimise it? [Admin Bar Minimiser Plugin](http://wordpress.org/extend/plugins/admin-bar-minimiser/)

Want to disable it selectively? [Admin Bar Disabler Plugin](http://wordpress.org/extend/plugins/admin-bar-disabler/) can do that.

Finally if you MUST turn it off…

To disable it, you can add this to your functions.php

```
/* Disable the Admin Bar. */
add_filter( 'show_admin_bar', '__return_false' );
```

or

```
/* Disable the Admin Bar. */
show_admin_bar(false);
```

or

```
/* Disable the Admin Bar. */
show_admin_bar(0);
```

OR use the [Disable Admin Bar](http://wordpress.org/extend/plugins/disable-admin-bar/) plugin.

FYI, if you put the plugin in a folder called mu-plugins (yes, you can do this on Single Site as well as MultiSite) then your users won’t be able to un-install it unless they go in via FTP. Just put the mu-plugins folder in the same level as themes and plugins (wp-content/mu-plugins) and copy the FILE (not the folder) for the plugin into there. Done.