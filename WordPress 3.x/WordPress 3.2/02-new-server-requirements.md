# NEW SERVER REQUIREMENTS

Be aware, [WordPress 3.2 has new requirements](http://wordpress.org/about/requirements/):

- PHP version 5.2.4 or greater
- MySQL version 5.0 or greater

If you have not yet upgraded and want to make sure you’re okay, please use [Ryan Duffís WordPress 3.2 Requirementís Check](http://wordpress.org/extend/plugins/wordpress-requirements-check/). Should your server not be ready, email your host:

> I run WordPress <http://wordpress.org/&gt; on my website and would like to upgrade to the latest version when itís released. It has the following requirements:
> 
> PHP 5.2.4 or greater
> 
> MySQL 5.0 or greater
> 
> Please make sure that my PHP and MySQL are up-to-date.

This may be a hassle, depending on how savvy your host is, as there’s really no good way to go from SQL 4 to 5 (this is SQL’s ‘fault’). Both PHP 5 and SQL 5 have been out for years and are stable tech, so if your host WON’T upgrade, look for a new host.

**Errors caused by PHP**

If your THEME or PLUGIN has PHP 4 specific code, things will break. Known issues related to this change:

**Missing class-json.php**

[From Dion Hulse](http://wordpress.org/support/topic/missing-class-jsonphp?replies=6#post-2165289)

> WordPress 3.2 required PHP 5.2.4 or later, class-json.php was included for compatibility with older versions of PHP only. It was removed here: http://core.trac.wordpress.org/changeset/17603
> 
> Unfortunately, Your theme will need to be updated, you may find that simply commenting out the include line will allow it to continue working if it was using the PHP json functions like any well built theme would have been.
> 
> Alternatively, Copy the json file into your themes folder, and modify the include line to reference the themes folder instead of WordPress’s.

Finally, if you’re having UX issues (where you can’t drag/drop widgets and similar), and you’ve already turned off all your plugins and changed to the default theme, you will need to go check if your PHP version has JSON installed. You may be able to add this on via cpanel, or you may have to ask your host to recompile it for you.