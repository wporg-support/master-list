# Known Issues

- [CloudFlare Plugin](https://wordpress.org/plugins/cloudflare/) breaks embeding posts. Deactivating the plugin will fix the problem. Another workaround is to disable the “Protocol rewriting” option for your site. Note that sites with the CloudFlare plugin protocol rewriting option won’t be able *to be embedded into* other sites, but they can embed *from* other sites (without the CloudFlare plugin) just fine. The company has been informed of this issue.
- The [Amazon S3 for WordPress with CloudFront plugin](https://wordpress.org/plugins/tantan-s3-cloudfront/) breaks thumbnails and other responsive images under WordPress 4.4. As this plugin has not been updated for 4 years, switch to an alternative, like [WP Offload S3](https://wordpress.org/plugins/amazon-s3-and-cloudfront/).
- Plesk Updates: There is a problem with Plesk’s provided WordPress 4.4 updater. If you use Plesk’s application updates, you’ll have to update via Dashboard -> Updates in your site’s Dashboard or [manually](https://codex.wordpress.org/Upgrading_WordPress_Extended).
- WP CLI – Needs to be upgraded to the latest release, otherwise it won’t work.
- JSON/REST API – Needs to be upgraded to the latest version of whatever branch you run to work.
- Avada theme – There is an issue with the theme version 3.8.8 and WordPress 4.4. Update to the latest version of Avada to fix the issue.
- Canvas Theme (for WooCommerce) – It seems to be throwing `error in category-template.php on line 1158`. Update to the latest version of Canvas to fix the issue.
- \[youtube=xxx\] Shortcodes no longer work – Known issue with the Jetpack plugin. Update to the latest version of Jetpack to fix the issue.
- The [Sliding Door theme](https://wordpress.org/themes/sliding-door/) suffers from a fatal error under WordPress 4.4. Update to the latest version of Sliding Door to fix the issue.
- [Ultimate Member plugin](https://wordpress.org/plugins/ultimate-member/) is causing some multisite network users to be unable to add new users from within subsite dashboards. Update to the latest version of Ultimate Member to fix the issue.
- WPML can experience an infinite redirect loop, likely caused by [#35031](https://core.trac.wordpress.org/ticket/35031). Update to the latest version of WPML to fix the issue.