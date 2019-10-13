# Troubleshooting WordPress 3.6 Master List

It’s that time again, kids! [Oscar](http://wordpress.org/news/2013/08/oscar/) is here. But OMGWTFBBQ!? WordPress 3.6 broke everything?

_**Don’t Panic!**_

This thread contains the known issues with plugins and themes found in 3.6. Please read this WHOLE topic and come back and check again later, as it will be updated.

Remember to be calm, be patient and be respectful. Volunteers are out here to TRY and help you, but we need your help too. ALL [forum rules](http://codex.wordpress.org/Forum_Welcome) still apply. You are just as important as everyone else.

If your post doesn’t show up right away, please be patient. With the higher than normal post volume, more people get erroneously flagged as spam. We’re working hard to keep the queue clear, but making multiple posts slows us down, as we have to go back and check if you already posted. Post one. If it shows up as ‘Anonymous’, we’ll fix it for you. Just wait.

- **Do** use proper capitalization (in titles or body). Punctuate your sentence properly and humanely, it helps us read.
- **Do** use descriptive subject lines (“All permalinks broken since 3.6” instead of “Augh! Help ASAP! This version is terrible!”)
- **Do** be patient. We know it sucks to be down, but we delete bumps on sight.
- **Do** make your own topic _unless_  you are using the same version of WordPress on the same physical server hosted by the same hosts with the same plugins, theme and configurations as the original poster (I know it’s weird, but it will be easier for us to help YOU that way)
- **Do** mark your topic as resolved when it’s fixed so we know not to come looking there anymore.
- **Do** remember you’re not alone.

If you’re upgrading from an older version of WordPress, you may want to read lists for [3.1][version-3.1], [3.2][version-3.2], [3.3][version-3.3], [3.4][version-3.4], and [3.5][version-3.5]. There are known issues with older themes and plugins, and they may not have been corrected.

Also keep in mind that not liking the direction of WordPress’s Admin Design does not a bug make. If you don’t like a feature, please don’t make a series of posts complaining about it. Look and see if someone already did, and post there, or consider joining the process earlier on (like in Beta or even test via SVN). What you’re seeing today is the result of months of work and testing, and unless something is outright broken, it’s highly unlikely to be changed.

Again, BEFORE you post:

Make sure you’ve read the entire [Master List](http://wordpress.org/support/topic/troubleshooting-wordpress-36-master-list) post – and the [New Features in 3.6 Codex Article](http://codex.wordpress.org/Version_3.6) – http://codex.wordpress.org/Version_3.6

Go to your own install’s about page – http://example.com/wp-admin/about.php – to see what’s new.

And then make sure you’ve tried…

- flushing any caching plugins you might be running, as well as server and/or **browser caches**.
- deactivating **all plugins** (yes, all) to see if this resolves the problem. If this works, re-activate the plugins one by one until you find the problematic plugin(s). If you can’t get into your admin dashboard, try resetting the plugins folder by FTP or PhpMyAdmin (read [“How to deactivate all plugins when you can’t log in to wp-admin”](http://codex.wordpress.org/FAQ_Troubleshooting#How_to_deactivate_all_plugins_when_not_able_to_access_the_administrative_menus.3F) if you need help). Sometimes, an apparently inactive plugin can still cause problems. Also remember to deactivate any plugins in the mu-plugins folder. The easiest way is to rename that folder to `mu-plugins-old`
- switching to the Twenty Twelve theme to rule out any theme-specific problems. If you can’t log in to change themes, you can remove the theme folders via FTP so the only one is `twentytwelve`. That will force your site to use it.
- manually upgrading. When all else fails, download a fresh copy of the latest.zip file of 3.6 (top right on this page) to your computer, and use that to copy up. You may need to delete the wp-admin and wp-includes folders on your server. Read the [Manual Update directions first](http://codex.wordpress.org/Updating_WordPress#Manual_Update).

[version-3.1]: http://wordpress.org/support/topic/troubleshooting-wordpress-31-master-list
[version-3.2]: http://wordpress.org/support/topic/troubleshooting-wordpress-32-master-list
[version-3.3]: http://wordpress.org/support/topic/troubleshooting-wordpress-33-master-list
[version-3.4]: http://wordpress.org/support/topic/troubleshooting-wordpress-34-master-list
[version-3.5]: http://wordpress.org/support/topic/troubleshooting-wordpress-35-master-list