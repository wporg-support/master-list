# MISSING OPTIONS IN POSTS

3.1 hides some screen options on posts & pages edit screens by default. Just turn on the ones you want.
More info here: http://ottopress.com/2011/wp-quickie-metaboxes/

Alternately, put this in your theme’s functions.php if you want the custom fields to show up by default ([from this thread](http://wordpress.org/support/topic/extra-fields-dissapeared-in-new-post?replies=7)):

```
// Change what's hidden by default
add_filter('default_hidden_meta_boxes', 'be_hidden_meta_boxes', 10, 2);
function be_hidden_meta_boxes($hidden, $screen) {
	if ( 'post' == $screen->base || 'page' == $screen->base )
		$hidden = array('slugdiv', 'trackbacksdiv', 'postexcerpt', 'commentstatusdiv', 'commentsdiv', 'authordiv', 'revisionsdiv');
		// removed 'postcustom',
	return $hidden;
}
```

(By the way, if you ever customized yours, that’s why they didn’t vanish. It only changed for people still using default.)