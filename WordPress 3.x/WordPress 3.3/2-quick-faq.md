# QUICK FAQ!

The following questions were culled from the alpha/beta forum as well as the wp-testers list.

__I can’t install a Plugin/theme! WordPress says “The package is corrupt or not in the correct format.”__

If you’re getting this from the official WordPress.org repositories, please email plugins[at]wordpress.org or contact http://lists.wordpress.org/mailman/listinfo/theme-reviewers to let people know.

If you’re getting this from an external site, it means they didn’t package the theme/plugin correctly. All themes and plugins should install into a folder (i.e. pluginname). Also all themes require a style.css. If you see this error, contact the site from which you got the installer and let them know.

__Admin menu doesn’t expand/collapse__

Actually it does, but on a per-section basis. This is not a bug, this is by design and will not be changed any time soon. The menus are now ‘flyout’ when you hover over them and will expand completely if you click on them.

If you’re desperate to expand all menus, there is a plugin: http://wordpress.org/extend/plugins/expanded-admin-menus/

__I lost my media upload buttons!__

No, they were just consolidated into one. You can upload all media types via the one button.

__I can’t turn off the Admin Bar__

You can disable it from showing on the front-end of your site, but not the admin area. This is by design, as the Admin Bar has replaced the admin page header from previous versions. Notice that your ‘Site Name’ no longer appears at the top of the page, and is now a part of the Admin Bar.

__My Admin bar is styled wrong/has no style/won’t format!__

You were probably using something like this to disable it:

```
wp_deregister_script('admin-bar');
wp_deregister_style('admin-bar');
```

Remove that from your theme and you’re GTG!

I’m getting weird java/js errors!

jQuery was changed to version 1.7.1 in WordPress core, which may cause problems with plugins and themes.  Do the needful and turn off your plugins and try the default theme first.

__I’m on Chrome and my admin-side looks all wrong!__

The Chrome extension _Send from Gmail (by Google)_ causes a javascript issue with makes the display on the admin-end look wrong. Turn it off and remove.

__I need to disable those cool feature pointers for my site!__

If you must… Add this to your functions.php:

```
remove_action( 'admin_enqueue_scripts', array( 'WP_Internal_Pointers', 'enqueue_scripts' ) );
```