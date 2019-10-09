# KNOWN ISSUES

_Endless notice to update the database_

If your dashboard is stuck telling you that you have to upgrade your database (or that you don’t) over and over, see if you’re running a cache like Redis, Memcached, or APC. You may need to flush that.

This particular issue is being discussed at https://core.trac.wordpress.org/ticket/27669

_Database times out on update_

If the DB upgrade fails or times out, it’s like because the wp_posts table is very large. Try to clear out revisions and optimize the database.

You can mitigate this risk by optimizing your database and removing revisions beforehand. Some plugins can help with this.

Eg. https://wordpress.org/plugins/better-delete-revision/

If you did not do that and you’re locked out of wp-admin, or simply want to directly run SQL lines, use the following –

```
DELETE a,b,c FROM wp_posts a LEFT JOIN wp_term_relationships b ON (a.ID = b.object_id)
LEFT JOIN wp_postmeta c ON (a.ID = c.post_id) WHERE a.post_type = 'revision'
```

Then run a DB optimize.

_Fatal Error with `Cannot redeclare get_avatar url()`_

This is generally caused by a theme that has not yet been updated to be compatible with WP4.2. You can either manually deactivate the theme by renaming it on the server (use [FTP](https://codex.wordpress.org/FTP_Clients) or another file manager to access your site files on the sever) to `mytheme.HOLD` – which should let you login again. Then check whether the theme has a recent update – if so, **update the theme** and that should fix the problem.

Alternatively, you can temporarily fix the error without removing the theme by editing that file. If you look at the error log it will tell you which line contains the error and which file. **First make a backup copy of the file in a safe place just in case editing the file goes wrong!** Then on the real file, comment out the entire section (function) that is causing the error by placing /* in front of the statement and */ immediately following it. This will exclude it from being processed.

Why this broke: This function was built into WordPress in 4.2, but was previously something that the theme author had to include. In 4.2 the exact same statement that you commented out is included in wp-includes/link-template.php.

_Site is Blank after Update_

If you were using [Twenty Ten](https://wordpress.org/themes/twentyten/), [Twenty Eleven](https://wordpress.org/themes/twentyeleven/), [Twenty Twelve](https://wordpress.org/themes/twentytwelve/), [Twenty Thirteen](https://wordpress.org/themes/twentythirteen/), [Twenty Fourteen](https://wordpress.org/themes/twentyfourteen/), or [Twenty Fifteen](https://wordpress.org/themes/twentyfifteen/) as your theme, and you received WordPress 4.2 by a hosting provider’s auto-update system, you may need to [manually install](https://codex.wordpress.org/Using_Themes#Adding_New_Themes_Manually_.28FTP.29) a new version of the theme.

Why this broke: Some hosting providers were distributing corrupt themes with their WordPress 4.2 update packages. This does not affect anyone who has updated WordPress via the Dashboard, updated manually via FTP/SFTP, or via a WordPress-powered auto-update mechanism.

_I’m on MySQL 5.5.14 or higher, but my database character set did not update to utf8mb4._

Follow [this guide](http://pento.net/2014/04/07/wordpress-and-utf-8/) to manually update your database character set and collation.

We’re still investigating this. It appears that the upgrade incorrectly required an instance of MySQLi. Please feel free to follow along at https://core.trac.wordpress.org/ticket/32127