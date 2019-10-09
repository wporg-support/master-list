# NOT A BUG

_**My layout is all weird on the Dashboard**_

Flush your cache. If you’re using server caches, or a plugin, flush them too, especially Memcached/APC stuff. They can be sticky. This includes Cloudflare and Pagespeed and Varnish. Anything that caches.

_**I’ve upgraded and the posts are not styled correctly**_

Check if you are running `mod_pagespeed` and if you are try disabling it to see if your posts render correctly.

_**My users are getting lots of password change emails for no seeming reason**_

Most likely, you are using some plugin that integrates your user accounts with accounts on some other system. That plugin is modifying user accounts on some sort of regular basis. It is likely doing so incorrectly, and causing WordPress to trigger the password change emails.

Get in contact with your plugin’s author, and give them this information:

> The password change email is triggered any time that the wp_update_user() function is called with a user_pass argument. If the plugin is not actually changing the password, then it needs to not update the user with a password field in the arguments array.
> 
> This is because whether or not you change the password, even to the same password, the database will be changed. WordPress doesn’t know the password, only a hash of it. And the same password can be hashed pretty much an infinite number of ways. So if you send it a user_pass, then it actually is rehashing it and updating the entry in the database.
> 
> So, please stop calling wp_update_user() with a user_pass field over and over again. Then no more emails will be sent. Instead, consider checking if the user password has actually changed before trying to change it. You can use the wp_check_password() function for that.

A TEMPORARY workaround to stop password reset emails is to put this line of code into a plugin on your site and activate it:

`add_filter('send_password_change_email', '__return_false');`