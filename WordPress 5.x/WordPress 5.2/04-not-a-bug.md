# Not a bug

Noteworthy and recurring scenarios users are encountering that are not actually bugs, but rather changed or new behaviors.

**I am unable to update: The update cannot be installed because WordPress 5.2 requires PHP 5.6.20 or higher.**

With WordPress 5.2 we increased the minimum PHP requirement for running the software. If you are seeing this message, check if your web-host has any documentation relating to upgrading your PHP version, or reach out to your server admin/support team for assistance in doing so.

**But I’m running PHP 5.6.3, isn’t that higher than PHP 5.6.20?**

No, PHP versions, and most software versions, do not follow how decimals work in math and such. In this case, PHP 5.6.20 is higher than PHP 5.6.3, because 20 is higher than 3.

**I don’t agree with Health Check’s score!**

That’s ok! Here are a few things to keep in mind:

1. Health Check will direct you to what the WordPress core developers consider to be the best case scenario for a WordPress installation.
2. Health Check cannot read your mind to determine the context behind your own decisions.
3. You do not need to win a perfect score in Health Check.
4. This is _your_ WordPress installation, which you can choose to run as you see fit.

**The site is experiencing technical difficulties.**

WordPress 5.2 introduces new protection from sites crashing due to bad code (also known as a White Screen of Death, or WSOD for short).

If your site crashes, the message above is shown, and an email is sent to the site admin with a way to log in and deactivate the plugin or theme causing problems, once that is done the site should start working again as expected.