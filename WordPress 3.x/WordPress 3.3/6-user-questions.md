> yourmy: After updating 20 or 30 sites to 3.2, I found out that the submit article body has disappeared, at least in ff and ie – only the title is shown for authors. Please check. Thanks!

> PHP Fatal error: Call to undefined function submit_button()

This sounds like not all the files were copied over correctly, I’d advice you attempt to perform a manual update as per the instructions in this codex article: http://codex.wordpress.org/Updating_WordPress#Manual_Update – Replace/overwrite the existing files. If you still have access to the Dashboard -> Updates page, you might be able to use the “Reinstall” function there to correct it. If neither of these help, deactivate your plugins, as one of those may be causing the issue.

> reh03jeene: please help me i have this message when i updated my wordpress site
> Warning: require_once(/home/bleys987/public_html/wp-includes/class-json.php) [function.require-once]: failed to open stream: No such file or directory in /home/bleys987/public_html/wp-content/plugins/tweet-this/tweet-this.php on line 145

The Tweet This plugin you’re running is not compatible with the latest version of WordPress. You’ll need to delete, or rename, the tweet-this plugin folder via FTP.

> fxmatics: So, why don’t our generous WP developers did not warn us about it before we upgrade? 🙁

The announcement post mentioned it, and the Automatic update would’ve prevented you from updating if you did not meet the system requirements. Furthermore, If you managed to update, You would’ve been locked out of WordPress all together with a system requirements message, not a partially operating WordPress install, Your issue sounds like a Plugin issue overriding the default jQuery that wordPress includes, try disabling your plugins and try again.

To everyone else: **Please make a new thread for your individual issue**