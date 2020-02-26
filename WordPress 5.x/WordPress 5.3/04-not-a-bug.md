# Not a bug

Noteworthy and recurring scenarios users are encountering that are not actually bugs, but rather changed or new behaviors.

**Elements in the admin area have borders now!?**

WordPress 5.3 ships with improved contrasts for the admin area. This is part of the project's ever ongoing work to improve accessibility.

**Some of the blocks in my editor look strange**

Some changes were made to the HTML used to display blocks. Although this won't affect any existing content, editing or writing new content where a theme or plugin is expecting certain styles may look strange. We recommend updating your themes and plugins, or reaching out to the authors if there are no updates available to address this change yet.

**The [Gutenberg](https://wordpress.org/plugins/gutenberg/) plugin stopped working for me**

With the release of WordPress 5.3, only version 6.6 or newer of the Gutenberg plugin is compatible, so please update the plugin and all should be good.

**Uncaught TypeError: $ is not a function**

Users may see the above if plugins or themes are trying to use the jQuery JavaScript library incorrectly. In WordPress version 5.2 or earlier, there was a bug in a part of the code that is used called `mediaelement.js`, this bug has been patched, and that means previous incorrect usage no longer works as expected.

More technical details can be found at https://core.trac.wordpress.org/ticket/48568

**Dates or times being incorrect, permalinks being off by a day, other weirdness related to “time”**

WordPress 5.3 received a significant upgrade to its date and time handling code. The previous code dated all the way back to over 10 years ago when PHP 4 was still supported. This was a significant chunk of code scattered all through the core of WordPress, and it was very slow and a drag on performance.

With 5.3, most of this code has been updated or replaced with saner PHP 5.6 compatible code. A lot of the legacy has been removed. However, some plugins and themes may have relied on the side effects of how this code previously operated.

For this reason, some plugins or themes may be doing incorrect things. One such thing would be to call the `date_default_timezone_set()` function in PHP. WordPress works by setting the default timezone to UTC and then performing its own calculations to adjust times. Setting the default timezone incorrectly to anything else will result in these calculations is incorrect. WordPress will be overcompensating the timezone adjustments.

For backward compatibility, it is crucial that plugins *not* change the default PHP timezone. The default timezone must be set to UTC at all times. Any problems you find with timezones or dates shifting is likely going to be a plugin or theme which is doing-it-wrong. This may not have mattered as much in previous versions of WordPress, but now that WordPress is using these newer functions more and less reliant on the old PHP 4 compatible code, then this is far more critical.

If you find a plugin or theme with a problem like this, please report it to their authors, or report it to the plugins team.
