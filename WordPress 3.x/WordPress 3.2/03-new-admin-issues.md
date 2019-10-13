# NEW ADMIN ISSUES

**Why is WordPress telling me my broswer is outdated/insecure?**

Because it is.

If you use a non-supported (or very old) browser like IE 6 or 7, or FireFox 3 or 4, WordPress will tell you, in your admin section, that this is out of date and you should upgrade. Yes, this is a nag screen. No, it’s not going away. Just upgrade if you can, or click dismiss if you cannot.

If you’re stuck on Windows 98, good news! Opera supported Windows 98 all the way up to 10.63 (released less than a year ago) and that can still be downloaded from http://www.opera.com/browser/download/?os=windows&list=all

**Where did the ‘create new post’ button go?**

There are “Add New” links everywhere now, next to the screen title, but more importantly, WordPress’s direction is to utilize the Admin Bar for these extra links.

**Where did my Network Admin Link Go!?**

It’s a dropdown now. Click on ‘Howdy, YOURNAME’ and it’ll show up.

**My site is set to private, but I don’t see that in the header anymore.**

That’s been removed from the header bar when it was resized. Right now it’s only viewable from your site’s dashboard, in the ‘Right Now’ section.

**I don’t like how the new admin section looks**

The dashboard’s appearance has been redesigned with future versions of WordPress in mind. It can be customized via plugins or CSS.

See http://codex.wordpress.org/Creating_Admin_Themes

**The Fullscreen button in the Visual editor is now missing!**

To fix the problem:

1. Deactivate (and preferably remove) the old “WordPress Automatic Upgrade” plugin.
2. Go to the Dashboard->Updates option in the menu.
3. On this new page, select to Re-install WordPress 3.2.1. It’ll spin a minute and redownload WordPress and install it over itself properly, fixing any missing or broken files.
4. Clear your browser cache. Your browser will have a copy of the bad Javascript files in memory, and until you clear them out, it won’t try to load them from the site again.
5. Reload the editor page. The full screen button is between the spell check button and the “kitchen sink” button.