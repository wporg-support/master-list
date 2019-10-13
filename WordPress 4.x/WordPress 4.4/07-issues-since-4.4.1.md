# Issues Since 4.4.1

_Remember!_ Any plugin or theme updates that happen right after 4.4.1 usually are related, so please update them asap.

- Pagination breaks if a static front page is set with a query to display posts on it, rather than setting a standard posts page. A trac ticket for this exists at https://core.trac.wordpress.org/ticket/35689
- cPanel users may find wp-admin blocked due to a recent update to their server’s mod_security rules. Please contact your hosting provider if you encounter this.

  **Technical Details**: Hosting providers who subscribe to Comodo WAF for their mod_security rules recently received an updated set of rules containing specifically rules #214620 and #214940, which are causing this problem.
  
  You may also find that the official rules, in particular #981004 now also triggers on the WordPress admin panel.
  
  Comodo is aware of the issue and working on a fix for their rules. The official mod_sec rules have also been reported for false positives, but it will be up to the hosting providers to apply these fixes.
  
  **A fix for this has also been included in WordPress 4.4.2**
- Static Front Pages and Maintenance Mode Plugins – In some cases, these cause an endless redirect loop. Basically if you use any kind of pretty permalinks AND have a static front page configured, the home page results in an infinite redirect loop. This appears to be caused by mixed case domain names in your settings.

  **Solution**: Go to `Settings > General` and make sure your siteurl ad home url are all lowercase (A Trac ticket for this exists at https://core.trac.wordpress.org/ticket/35364 to look into the behavior and resolutions)
  
  **This has been fixed in WordPress 4.4.2**
- If posts belonging to a custom post type are set to display on the posts page, and the posts page is set as the front page, with pretty permalinks, pagination no longer works (i.e. /page/2, /page/3) — instead those links redirect back to the front page. There is a working patch in https://core.trac.wordpress.org/ticket/35344
  
  **This has been fixed in WordPress 4.4.2**

**Issues with HTTPS loops**

Some plugins force HTTPS/SSL for security and by design. When there’s a miss-match with settings, the new cannonical URL rules can cause a site to get ‘stuck’ looping between http and https. If you’re using any of the following plugins, you will need to change a setting:

- [WooCommerce](https://wordpress.org/plugins/woocommerce/) – WordPress falls into a redirect loop when the home/site URLs are set to https, and Woo is set to serve https on checkout but redirect to http after. DO NOT CHECK THAT BOX!!! Here’s an image to explain: https://cloudup.com/cm2EtBJvOzn **Update to the latest version of WooCommerce to officially fix the issue.**
- [WordPress HTTPS](https://wordpress.org/plugins/wordpress-https/) – You may fall into a https loop if you have https set to ‘Force SSL Exclusively’. Uncheck that box if so.
- [SSL Insecure Content Fixer](https://wordpress.org/plugins/ssl-insecure-content-fixer/) – Deactivate and reactivate should clear out the cache for this one. If that doesn’t work, delete the plugin and reinstall.