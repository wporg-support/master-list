# MISC. OTHER ERRORS

Older versions of Memcache may have issues, however there has not been enough testing of this one.

Using the same names for tags and categories remains problematic, though this has always been a bit sketchy.

From godlikemouse:

> If you run into the problem where your toolbar disappears from your WYSIWYG editor as well as the WYSIWYG editor not working at all, try this.
> 
> go to your wp-includes/js/tinymce/langs and create a symbolic link to wp-langs-en.js as en.js.
> 
> `ln -s wp-langes-en.js en.js`
> 
> Looks like someone forgot to rename a file on the upgrade.

From madpress

> Using a pre_get_posts filter in functions.php (to merge posts and custom post types) worked fine with 3.0.x, but seems to require an explicit is_admin check since 3.1, e.g.
> 
> ```
> if ( !is_admin() ) {
> add_filter( 'pre_get_posts', 'funky_get_posts' );
> function funky_get_posts( $query ) {
>	 if ( is_home() || is_archive() || is_search() || is_paged() )
> 		$query->set( 'post_type', array( 'post', 'live-shows' ) );
>	 return $query;
> }
> }
> ```
> Not using this is_admin check results in a warning (“Warning: Illegal offset type in isset or empty in /home/my-site/public/wp-includes/post.php on line 811”) and messes up the admin pages for custom post types.
> 
> see: http://osdir.com/ml/wordpress-hackers/2010-07/msg00619.html