# FATAL ERRORS
Fatal error in the output means either your theme doesn’t like 3.1, you have a plugin that doesn’t like 3.1, or you have an incomplete upgrade.

hertz suggests this if you have a fatal error with MultiSite:

> 1. add define(‘WP_ALLOW_REPAIR’, true); to your wp-config.php
> 2. open [your site]/wp-admin/maint/repair.php
> 3. if everything fine in step 2, go to step 4 or try to solve appear in repair page(step 2).
> 4. change your plugins and themes folder name to something
> 5. delete wp-admin, wp-include and all files in your wordpress root except wp-config.php.
> 6. add new update package in your wordpress installation.
> 7 go to phpmyadmin and find all plugin related tables, keys and value and drop all.
> 8. open again [your site]/wp-admin/maint/repair.php
> 9. try to upgrade your network