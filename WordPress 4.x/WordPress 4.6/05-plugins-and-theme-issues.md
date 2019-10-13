# Plugin and Theme Issues

_Genesis (StudioPress)_ users may experience a fatal error if they have not updated their theme yet, updating to version 2.3.1 or later ensures compatibility with WordPress 4.6

_Thesis 1.8_ (which is very old anyway) and its child themes may see the following error:
```
Error message is Fatal error: Cannot redeclare the_post_thumbnail_caption() (previously declared in /home/USER/public_html/wp/wp-includes/post-thumbnail-template.php:244) in /home/USER/public_html/wp/wp-content/themes/thesis_18/custom/custom_functions.php on line 617
```

This is due to a poorly named (non prefixed) function which was added post install (that is – it’s NOT in core thesis, but a significant number of people have added it to the main theme). You can either rename the calls to `the_post_thumbnail_caption` or upgrade to Thesis 2.x. Also please remember – DON’T edit your parent themes directly 🙂 Make child themes.