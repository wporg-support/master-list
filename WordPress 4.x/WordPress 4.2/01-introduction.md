# READ THIS FIRST - WordPress 4.2 Master List

Hooray! [Powell is here](https://wordpress.org/news/2015/04/powell/)! But OMGWTFBBQ!? WordPress 4.2 broke everything?

_**Don’t Panic!**_

Before you go any further, make sure you’ve updated to the latest point release (currently 4.2.2). Still having problems? Okay, read on!

This thread contains the known issues with plugins and themes found in 4.2. Please read this WHOLE topic and come back and check again later, as it will be updated.

Remember to be calm, be patient and be respectful. Volunteers are out here to try and help you, but we need your help too. All of the normal [forum rules](http://codex.wordpress.org/Forum_Welcome) still apply. Remember, you are just as important as everyone else.

If your post doesn’t show up right away, please be patient. With the higher than normal post volume, more posts get flagged as spam by our auto-spam tool. We’re working hard to keep the queue clear, but making multiple posts slows us down, as we have to go back and check if you already posted. Post once.

- **Do** use proper capitalization in post titles and body. Punctuate your sentence properly and humanely, it helps us read.
- **Do** use descriptive subject lines. “All permalinks broken since 4.2” is much better than “Augh! Help ASAP! This version is terrible!”
- **Do** describe the problem clearly. Explain what you’re seeing, include error messages and link to screenshots if needed. Linking to your site, if the problem is on the front-end, also helps.
- **Do** be patient. We know it sucks to be down, but posting multiple times doesn’t get you help any faster.
- **Do** make your own topic _unless_ you are using the exact same version of WordPress on the same physical server hosted by the same hosts with the same plugins, theme and configurations as the original poster. You may find it weird, but it will be easier for us to help you specifically if you have your own topic.
- **Do** mark your topic as resolved when it’s fixed so we know not to come looking there anymore.
- **Do** remember you’re not alone.

Also keep in mind that not liking the direction of WordPress’s design does not a bug make. If you don’t like a feature, please don’t make a series of posts complaining about it. Look and see if someone already did, and post there, or consider joining the process earlier on (like in Beta or even test via SVN). What you’re seeing today is the result of thousands of hours of work and testing, and unless something is outright broken, it’s highly unlikely to be changed.

Again, **before** you post:

Make sure you’ve read the entire [Master List](https://wordpress.org/support/topic/read-this-first-%E2%80%93-wordpress-42-master-list) post – and the [New Features in 4.2 Codex Article](http://codex.wordpress.org/Version_4.2#What.27s_New) – http://codex.wordpress.org/Version_4.2

Go to your own install’s about page – `http://example.com/wp-admin/about.php` – to see what’s new.

And then make sure you’ve tried…

- **Troubleshooting with your browser**. Your browser can help you identify JavaScript issues or conflicts and [this article can assist you in doing that diagnosis](http://codex.wordpress.org/Using_Your_Browser_to_Diagnose_JavaScript_Errors). This could help identify Visual Editor issues as well.
- Flushing any caching plugins you might be running, as well as server and/or **browser caches**.
- Deactivating **all plugins** (yes, all) to see if this resolves the problem. If this works, re-activate the plugins one by one until you find the problematic plugin(s). If you can’t get into your admin dashboard, try resetting the plugins folder by [FTP](http://codex.wordpress.org/FTP_Clients) or PhpMyAdmin (read [“How to deactivate all plugins when you can’t log in to wp-admin”](http://codex.wordpress.org/FAQ_Troubleshooting#How_to_deactivate_all_plugins_when_not_able_to_access_the_administrative_menus.3F) if you need help). Sometimes, an apparently inactive plugin can still cause problems. Also remember to deactivate any plugins in the mu-plugins folder. The easiest way is to rename that folder to `mu-plugins-old`
- Switching to the Twenty Fifteen theme to rule out any theme-specific problems. If you can’t log in to change themes, you can remove the theme folders via [FTP](http://codex.wordpress.org/FTP_Clients) so the only one is `twentyfifteen`. That will force your site to use it.
- Manually upgrading. When all else fails, download a fresh copy of the latest.zip file of 4.2 (top right on this page) to your computer, and use that to copy up. You may need to delete the wp-admin and wp-includes folders on your server. Read the [Manual Update directions first](http://codex.wordpress.org/Updating_WordPress#Manual_Update).