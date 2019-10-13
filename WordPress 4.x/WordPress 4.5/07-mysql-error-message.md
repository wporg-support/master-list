# MySQL error messages

Previous to WordPress 4.5, error messages and other warnings that originated in the PHP and MySQL database systems were being suppressed, or hidden from the users. On the whole, this is not a great solution for long term, because while the systems usually “work” even with these types of errors, it is better to find and fix errors when they exist.

So, WordPress 4.5 removed the error suppression code from the database system. This may cause assorted warnings that you did not previously see. It is important to understand that WordPress 4.5 did not *cause* these warnings, it simply stopped hiding them from you like previous versions did. The errors were already there.

It is also important to note that these particular issues are rare. Uncommon. They only happen with very specific conditions, usually in older hosting environments. The easiest way to fix them may be to simply have your host update your hosting service to a newer server, or to migrate to a better hosting system in some manner.

Here’s some of the types of warnings we’ve seen so far, with instructions on how to fix them. Note that fixing these types of issues in your server configurations may not be the easiest thing in the world. You may need help from your hosting service.

**Warning: mysqli_real_connect(): The server requested authentication method unknown to the client \[mysql_old_password\]**

Your MySQL server appears to be old, or is otherwise using “old passwords”. The mysqli client does not support old passwords. WordPress uses the mysqli client preferentially when PHP 5.5 or higher is available on the hosting software.

Ideally, you need to modify your MySQL server to use the “new password” format. This isn’t really “new”, it’s been around for 10 years, however some servers are configured to use old password hashes still, to this day.

There’s various articles on how to do this around the web, however, you will probably need to ask your host to do this for you, or to migrate your database to a newer MySQL server instead. However, if you have the ability to fix your server, here are some example articles on the topic:

https://stackoverflow.com/questions/13706463/authentication-method-mysql-old-password-not-supported
http://code.openark.org/blog/mysql/upgrading-passwords-from-old_passwords-to-new-passwords

That would be the correct way to do things. It is also more secure. You want your MySQL server to be using better password hashes.

If you need a quick-fix instead, then add this to your wp-config.php file. This will force WordPress to use the old, deprecated mysql client. You should avoid this long term, since the mysql client will not be supported in later versions of PHP.

`define('WP_USE_EXT_MYSQL', true);`

**Warning: mysql_connect(): Headers and client library minor version mismatch**

This is caused by a mismatch between the mysql libraries that your PHP installation is using and the mysql client libraries installed on your actual system. This can be resolved by switching PHP to use the “ND” (Native Driver) version of these libraries. These ND versions have the client included with the library and so don’t have that external dependency that can cause this version mismatch error.

How you switch to using the ND versions depends on your hosting system. If you’re on a shared host, then you need to tell them about it and have them fix it for you.

The most recommended fix would be to see if your hosting provider provides a newer version of PHP. Most providers have some means for you to select the version of PHP that you want to use. Simply updating your PHP version to a more recent one will often fix the issue. We recommend selecting the latest version of PHP available to you. This would usually be PHP 5.6 or PHP 7.0. (Bonus! Using a newer PHP makes your website run *much* faster too!)

If you have access to a cPanel for your hosting system, then check in the PHP Selector that you are using the nd_mysql and nd_mysqli libraries, and not the basic mysql and mysqli ones.

If you have control over the server, then you can use your preferred package installation system to remove the php5-mysql packages in favor of the php5-mysqlnd ones instead.

More information:
https://stackoverflow.com/questions/10759334/headers-and-client-library-minor-version-mismatch

> [WP4.5 upgrade mysql_connect() error](https://wordpress.org/support/topic/wp45-upgrade-mysql_connect-error/)