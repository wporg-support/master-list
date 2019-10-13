# Not a Bug

The following features changed behavior.

**Linking in Posts**: The link interface has changed. Now it’s a smaller, inline tool that does a better search. Just start typing in your existing post title, and it will show up. If you miss the old interface, click the gear icon.

**Formatting Shortcuts**: We already had lists and headings. Now we’ve included horizontal lines and code too. Your text magically changing is intentional.

**Image Quality**: Yes, we changed it. It shouldn’t impact most people, but we’re trying to make WordPress render faster. If you happen to be a photoblogger and desperately need it back, please check out the following plugins

- https://wordpress.org/plugins/wp-resized-image-quality/
- https://wordpress.org/plugins/jpg-image-qualitycompression/

You can, of course, add code like this to your site, however we think most people would like that slider more than guesswork. Just change 100 to the percentage you’d like to render as:
```
add_filter( 'jpeg_quality', 'worg_support_image_quality' );
function worg_support_image_quality() {
    return 100;
}
```

The old setting was 90 and the new is 82. (Please read [the proposal to fully understand the research and decision](https://make.wordpress.org/core/2016/02/22/proposal-increase-the-default-image-compression-in-wordpress/).)

**Embedding WordPress**: You can now embed a front page of a WordPress site in another WordPress site.

The following features are new, but may not show up on all sites.

**Custom Logo**: This feature is only available on themes that have implemented it. If you don’t see it, check out TwentySixteen.

**Warning messages where there were no warning messages before**: The WP Database code no longer suppresses warning messages. This is intentional, in an effort to help users and hosts find problems with their configurations. However, normal production systems should not be displaying warning messages in any case. Check your wp-config.php file and make sure that the WP_DEBUG setting is set to “false”, and also check that your hosting system has the PHP “display_errors” setting disabled. Debug messages are for testing, not live systems.
