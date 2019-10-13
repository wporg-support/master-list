# KNOWN ISSUES

_**Media doesn’t remember what I want it to be linked to**_

Prior to 4.0, the last “Linked to” option chosen when inserting media persisted as a default for future inserts until it was next changed. This was handy for bloggers who always linked to the attachment page or chose a custom link when inserting media. In 4.0, “Media File” is now a persistent default for “Linked to,” and changes to it do not “stick” as they did prior to 4.0.

There is a ticket for this: https://core.trac.wordpress.org/ticket/23847

_**PHP Fatal error: Class ‘WP_Session_Tokens’ not found**_

This is a symptom of an incomplete update. Specifically, the “root” files were not updated. If you were using any form of non-standard update method or script, please remove it or do not use it in the future. The built-in one-click updater in WordPress will not cause this issue, or it will prevent the error from occurring and breaking your site.

To fix this error, you need to perform a manual upgrade, and be certain that ALL files are updated. Instructions can be found here:
http://codex.wordpress.org/Updating_WordPress#Manual_Update

Quick version: Download a fresh copy of WordPress from this site. Then replace all the files in your installation with the files from this ZIP. However, do not delete the files in your install first. Things like the wp-content folder and the wp-config.php file must remain intact. Only replace the files in the wp-includes, wp-admin, and the root directories. If in doubt, please follow the instructions on the codex exactly.

_**Installed plugins disappear:**_

Some users are experiencing a problem with installed plugins disappearing after updating to WordPress 4.0. The cause for this is not yet known but an active ticket can be found here: https://wordpress.org/support/topic/40-upgrade-makes-all-plugins-disappear

_**Fatal error: Call to undefined function hash() in \[directories\]/wp-includes/session.php on line 64**_

Some users are experiencing the above error when logging in after updating to WordPress 4.0. To correct the issue, ask your hosting provider to install PHP’s Hash module. Initial discovery: http://wordpress.org/support/topic/updated-and-got-fatal-arro