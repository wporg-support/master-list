# FOR DEVELOPERS

So your theme/plugin is breaking?

For themes, we recommend perusing http://make.wordpress.org/themes for any WordPress 3.4-related Theme issues. The biggest one is the handling of custom backgrounds and custom headers. There’s not a whole lot else.

Helpful links:

- http://make.wordpress.org/themes/2012/04/06/updating-custom-backgrounds-and-custom-headers-for-wordpress-3-4/
- http://sabreuse.com/flexible-headers-in-wordpress-3-4-themes/
- http://ottopress.com/2012/how-to-leverage-the-theme-customizer-in-your-own-themes/
- http://wpdevel.wordpress.com/2012/06/07/wordpress-3-4-field-guide-for-developers/

By the way, if you get a lot of weird warnings and you’re _not_ a developer, go into your wp-config.php file and make sure that you’ve got `define('WP_DEBUG', false);` set 🙂 You don’t need it if you’re not debugging.