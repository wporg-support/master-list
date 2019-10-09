# KNOWN PLUGINS THAT WILL MESS YOU UP!

These plugins have been reported as either breaking your whole site, or simply NOT working on WP 3.1

Many MAY have fixes at this point, so always check the plugin page and see if there’s a new version first.

- Advanced Permalinks
- Cforms (by delicious day) – Upgrade to the latest version to correct
- Event Espresso and Easy Toolbox conflict, making it impossible to drag/drop widgets.
- Facebook integration plugin
- Facebook Like Button
  - [WordPress Facebook Like Plugin](http://wordpress.org/extend/plugins/wordpress-facebook-like-plugin/) compatible with WP 3.1
- Featured Content Gallery
- FT Signature Manager
  - causing an error message on the Visual Post editor that says “you do not have permission to do this”
- Global Translator (maybe because of qTranslate)
- Grooveshark prevents the ability to upload/insert images into posts. The button to upload an image is visible, but doesn’t actually do anything.
- Multipage Toolkit. See: [this post for details](http://wordpress.org/support/topic/upgraded-to-31-now-my-permalinks-dont-work?replies=38#post-1958820)
- [multiple-post-thumbnails](http://wordpress.org/extend/plugins/multiple-post-thumbnails/)
  - multiple-post-thumbnails has been updated to 0.5 which updates the readme and FAQ to fix a problem when upgrading caused by the sample code in the readme not using a check for class_exists before using the class.
- Post Editor Buttons ( http://wordpress.org/extend/plugins/post-editor-buttons/ )
- qtranslate seems to fail on 3.1 as well (this may affect many plugins)
- Rich Category Editor – It isn’t displaying any tinyMCE buttons
- Scissors Plugin (breaks TinyMCE)
- Simple Sidebar Share Widget
- Simple Tags (uncheck “Active tags for page” ) – This has been updated for 3.1!
- Theme My Login
- TinyMCE advanced – It works but does’t seem to be using the new link to post feature.
- op Level Categories (try switching to [FV Top Level Categories BETA version](http://foliovision.com/seo-tools/wordpress/plugins/fv-top-level-categories))
- Twitter Tools
- Visitor-Maps and Who’s Online
- P Auto Tagger
- [WP Footer Ad Plugin](http://www.stefandes.com/wordpress-plugin/wp-footer-ad/) breaks the Edit Post page in the admin area with a jQuery conflict.
- WP Hive [Fixed! Read the notes](http://wordpress.org/support/topic/upgrade-to-31-wp_cache_get-issue?replies=25#post-1977361)
- WP No Category Base – [Now compatible with 3.1 – Mar 7](http://wordpress.org/extend/plugins/wp-no-category-base/)
- WP-Stats-Dashboard
  - visual editor broken
  - couldn’t insert media into posts
  - couldn’t add tags to posts.
- Custom Post Type Archives: interferes with contextual help
