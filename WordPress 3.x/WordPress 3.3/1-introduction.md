#Troubleshooting WordPress 3.3 – Master List

Horray! [Sonny is here](http://wordpress.org/news/2011/12/sonny/)! But OMGWTFBBQ!? WordPress 3.3 broke everything?

Don’t Panic!

This thread contains the known issues with plugins (and, yes, [in core](http://wordpress.org/support/topic/troubleshooting-wordpress-33-master-list?replies=5#post-2496392)) found in 3.3. Please read this WHOLE topic and come back and check it later, as it will be updated.

Remember to be calm, be patient and be respectful. Volunteers are out here to TRY and help you, but we need your help too. ALL [forum rules](http://codex.wordpress.org/Forum_Welcome) still apply. You are just as important as everyone else.

If your post doesn’t show up right away, please be patient. With the higher than normal post volume, more people get erroneously flagged as spam. We’re working hard to keep the queue clear, but making multiple posts slows us down, as we have to go back and check if you already posted. Post one. If it shows up as ‘Anonymous’, we’ll fix it for you. Just wait.

- **Don’t** use excessive caps (in titles or body). Punctuate your sentence properly and humanely.
- **Do** use descriptive subject lines (“All permalinks broken since 3.3” instead of “Augh! Help ASAP! This version is terrible!”)
- **Don’t** bump your posts (they will be deleted on sight)
- **Do** make your own topic unless your problem is 100% exactly the same as someone elses (it will be easier for us to help YOU that way)
- **Don’t** post in topics marked “Resolved” (we don’t look at them).

If you’re upgrading from an older version of WordPress, you may want to read [Troubleshooting WordPress 3.1 – Master List](http://wordpress.org/support/topic/troubleshooting-wordpress-31-master-list) and [Troubleshooting WordPress 3.2 – Master List](http://wordpress.org/support/topic/troubleshooting-wordpress-32-master-list). There are known issues with older themes and plugins, and they may not have been corrected.

Also keep in mind that not liking the direction of WordPress’s Admin Design does not a bug make. If you don’t like a feature, please don’t make a series of posts complaining about it. Look and see if someone already did, and post there, or consider joining the process earlier on (like in Beta or even test via SVN). What you’re seeing today is the result of months of work and testing, and unless something is outright broken, it’s highly unlikely to be changed.

Again, BEFORE you post:

> Make sure you’ve read the entire [Master List](http://wordpress.org/support/topic/troubleshooting-wordpress-33-master-list) post and the [New Features in 3.3 Post](http://wordpress.org/news/2011/12/sonny/).
> 
> Go to your own install’s about page – http://domain.com/wp-admin/about.php – to see what’s new.
> 
> And then make sure you’ve tried…
> 
> – flushing any caching plugins you might be running, as well as server and/or browser caches.
> 
> – deactivating all plugins (yes, all) to see if this resolves the problem. If this works, re-activate the plugins one by one until you find the problematic plugin(s). If you can’t get into your admin dashboard, try [resetting the plugins folder](http://codex.wordpress.org/FAQ_Troubleshooting#How_to_deactivate_all_plugins_when_not_able_to_access_the_administrative_menus.3F) by FTP or PhpMyAdmin. Sometimes, an apparently inactive plugin can still cause problems. Also remember to deactivate any plugins in the [mu-plugins](http://codex.wordpress.org/Create_A_Network#WordPress_Plugins) folder. The easiest way is to rename that folder to `mu-plugins-old`
> 
> – switching to the Twenty Eleven theme to rule out any theme-specific problems. If you can’t log in to change themes, you can remove the theme folders via FTP so the only one is `twentyeleven`. That will force your site to use it.
> 
> – manually upgrading. When all else fails, download a fresh copy of the latest.zip file of 3.3 (top right on this page) to your computer, and use that to copy up. You may need to delete the wp-admin and wp-includes folders on your server. Read the [Manual Update](http://codex.wordpress.org/Updating_WordPress#Manual_Update) directions first!