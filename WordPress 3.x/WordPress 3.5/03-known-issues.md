# KNOWN ISSUES

_jquery_

Plugins and themes which use their own jQuery without properly compensating for WP’s will break. This isn’t new by any means. In fact, we’ve always said that replacing or overriding jQuery will bust things, and we don’t let people do it anymore in plugins or themes hosted here. That doesn’t stop people from doing it, though.

We’ve come up with some awesome directions to help you debug your jQuery issues: http://codex.wordpress.org/Using_Your_Browser_to_Diagnose_JavaScript_Errors

Don’t worry, if that was greek to you, do the usual turning off plugins and switching themes to figure out which one it is, and then tell the dev ‘Hey, you’re `doing_it_wrong()` and breaking things!’

In all cases, make sure you’re using the latest version of themes and plugins. For example, [TwentyTen](http://wordpress.org/extend/themes/twentyten) and [TwentyEleven](http://wordpress.org/extend/themes/twentyeleven) themes got an upgrade. Also many plugins have updated and will now work with 3.5. Make sure you upgrade them first before coming for help.

_mod_pagespeed_

On some hosting environments, aggressive settings for the “mod_pagespeed” addon can break the javascript code and cause scripts to not be able to function. This can cause many problems, such as widgets not working, menus not being draggable, the customizer not working, or the media screens not being available.

To fix the issue, you will need to disable mod_pagespeed, or adjust its settings to not take effect in the wp-admin directories. You may need to ask your hosting service for help on how to do this.

_PerishablePress “5G” blacklist_

If you’ve ever added the [5G blacklist](http://perishablepress.com/5g-blacklist-2012/) to your .htaccess file, then it will break the Javascript on WordPress 3.5. **Get the updated 5G blacklist here: http://perishablepress.com/5g-blacklist-2013/ that works with 3.5+**