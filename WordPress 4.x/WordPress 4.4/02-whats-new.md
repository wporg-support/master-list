# What’s New:

- [Twenty Sixteen is the new default theme.](https://wordpress.org/themes/twentysixteen/)
- Externally embeddable. WordPress 4.4 will now act as an oEmbed provider for posts. [This can be disabled with a plugin](https://wordpress.org/plugins/disable-embeds/).
- [Responsive images support](https://make.wordpress.org/core/2015/11/10/responsive-images-in-wordpress-4-4/) This will display alternate size images for different view sizes in the browser via the srcset attribute. You don’t need to worry about anything. While your existing images won’t be ‘converted’ they also don’t need to be as the code is really smart and uses the image sizes you already have rather than make new ones. If you **want** to regenerate your images to use the new `medium-large` size, you can use one of the existing plugins (e.g. the [Regenerate Thumbnails plugin](https://wordpress.org/plugins/regenerate-thumbnails/)).
- [Changes to the comment form layout.](https://make.wordpress.org/core/2015/09/25/changes-to-fields-output-by-comment_form-in-wordpress-4-4/)
- REST API support – You really want to use the [REST API Plugin](https://wordpress.org/plugins/json-rest-api/) if you want to use the API. If you were already using it, please upgrade to either 1.2.4 for the v1 branch or beta8 for v2 so things continue to work.
- Term Meta – It’s awesome! the term meta functions will return a WP_Error object if the term has not been split.

**What’s Changed:**

- [Improvements to the taxonomy component of WordPress.](https://make.wordpress.org/core/2015/10/23/4-4-taxonomy-roundup/)
- [Headings in the admin have changed, your plugin page headings may not have](https://make.wordpress.org/core/2015/10/28/headings-hierarchy-changes-in-the-admin-screens/) (but that shouldn’t break anything).
- [create_empty_blog() and get_admin_users_for_domain() in multisite have been deprecated](https://make.wordpress.org/core/2015/10/28/multisite-focused-changes-in-4-4/)