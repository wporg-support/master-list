# Not a bug

Noteworthy and recurring scenarios users are encountering that are not actually bugs, but rather changed or new behaviors.

**Elements in the admin area have borders now!?**

WordPress 5.3 ships with improved contrasts for the admin area. This is part of the project's ever ongoing work to improve accessibility.

**Some of the blocks in my editor look strange**

Some changes wee made to the HTML used to display blocks. Although this won't affect any existing content, editing or writing new content where a theme or plugin is expecting certain styles may look strange. We recommend updating your themes and plugins, or reaching out to the authors if there's no updates available to address this change yet.

**The [Gutenberg](https://wordpress.org/plugins/gutenberg/) plugin stopped working for me**

With the release of WordPress 5.3, only version 6.6 or newer of the Gutenberg plugin is compatible, so please update the plugin and all should be good.

**Uncaught TypeError: $ is not a function**

Users may see the above if plugins or themes are trying to use the jQuery JavaScript library incorrectly. In WordPress version 5.2 or earlier, there was a bug in a part of the code that is used called `mediaelement.js`, this bug has been patched, and that means previous incorrect usage no longer works as expected.

More technical details can be found at https://core.trac.wordpress.org/ticket/48568
