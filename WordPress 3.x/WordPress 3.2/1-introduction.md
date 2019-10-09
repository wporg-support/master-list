# Troubleshooting WordPress 3.2 – Master List

So OMGWTFBBQ!? WordPress 3.2 broke everything?

**Don’t Panic!**

First, upgrade to 3.2.1 (yes, we know). Then remember to be calm, be patient and be respectful. Volunteers are out here to TRY and help you, but we need your help too. ALL [forum rules](http://codex.wordpress.org/Forum_Welcome) still apply. You are just as important as everyone else.

- Don’t use all caps (in titles or body)
- Use descriptive subject lines (“All permalinks broken since 3.2” instead of “AUGH! HELP! This version is terrible!”)
- Don’t bump your posts (they will be deleted on sight)
- Make your own topic (it will be easier for us to help YOU that way)

BEFORE you post:

Have you tried:

– deactivating **all plugins** (yes, all) to see if this resolves the problem. If this works, re-activate the plugins one by one until you find the problematic plugin(s). Don’t forget the ones in mu-plugins. If you can’t get into your admin dashboard, try [resetting the plugins folder](http://codex.wordpress.org/FAQ_Troubleshooting#How_to_deactivate_all_plugins_when_not_able_to_access_the_administrative_menus.3F) by FTP or PhpMyAdmin. Sometimes, an apparently inactive plugin can still cause problems.

– switching to the Twenty Eleven theme to rule out any theme-specific problems.

– manually upgrading. When all else fails, download a fresh copy of the latest.zip file of 3.2 (top right on this page) to your computer, and use that to copy up. You may need to delete the wp-admin and wp-includes folders on your server. Read the [Manual Update](http://codex.wordpress.org/Updating_WordPress#Manual_Update) directions first!