# Core Changes

**Auto-updates for plugins and themes**

With WordPress 5.5, you will now be able to easily enable automatic updates for plugins and themes (if your site is set ot allow them, some hosts may handle this for you, and the option may then not be available to you).

Although the functionality for automatic updates have existed since [WordPress 3.7](https://wordpress.org/support/wordpress-version/version-3-7/), there is now a way to turn them on or off with relative ease, all from within your WordPress dashboard.

[Learn more about the new auto-update feature](https://make.wordpress.org/core/2020/07/15/controlling-plugin-and-theme-auto-updates-ui-in-wordpress-5-5/).

 
**The block editor has received numerous updates**
 
As with any major release of WordPress in the past year, the block editor has seen many updates which are included in this release (a total of 10 releases of the [Gutenberg plugin](https://wordpress.org/plugins/gutenberg/) are included).
 
[Learn more about the changes to the block editor](https://make.wordpress.org/core/2020/07/30/wordpress-5-5-field-guide/#blockeditor).
 
 
**Lazy-loading of images**
 
Media is an integral part of most websites these days, and as your internet browser improves, so does the technology available to improve the experience for your website visitors.
 
With this release, native lazy-loading (images will not be downloaded to your visitors device until they are needed) will be available by default for any sites using the media features WordPress have made available to theme and plugin developers.
 
[Learn more about lazy-loading in WordPress](https://make.wordpress.org/core/2020/07/14/lazy-loading-images-in-5-5/).
 
 
**All websites now come with a sitemap**

Sitemaps, a tool often used by search engines to discover what content exists on a website, so that they can more effectively index the site, are now built into WordPress.
 
[Learn more about the new sitemap feature](https://make.wordpress.org/core/2020/07/22/new-xml-sitemaps-functionality-in-wordpress-5-5/).


**jQuery Migrate is disabled by default**
 
jQuery Migrate, a tool which WordPress has bundled, and enabled by default, for many years, has now been turned off by default.
 
This is a tool intended to help developers in a transitional period, when jQuery (a framework for writing JavaScript code) was upgraded and removed some features.
 
In the time since it was created, the jQuery project has received many updates, and as WordPress prepares to make the transition to updating as well, this was a required first step to make sure plugins and themes are up to date.
 
If your plugins or themes has been negatively impacted by this change, and no update is available at this time, there is a [jQuery Migrate Helper plugin](https://wordpress.org/plugins/enable-jquery-migrate-helper/), which will re-enable the migration tool, and provide you with information about what plugin or theme might be misbehaving. 
 
[Read about the roadmap for updating jQuery](https://make.wordpress.org/core/2020/06/29/updating-jquery-version-shipped-with-wordpress/).