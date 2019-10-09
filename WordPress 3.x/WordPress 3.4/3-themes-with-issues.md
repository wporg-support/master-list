# THEMES WITH ISSUES

In all cases, make sure you’re using the latest version of the theme. For example, TwentyTen and TwentyEleven got an upgrade. Make sure you upgrade them first before coming for help.

_Problem_: You get the following error — `Fatal error: Class 'WP_Theme' not found in`
_Solution_: Reinstall WP. The `class-wp-theme.php` file is included by default. This could only really happen if they get an updated `wp-includes/theme.php` file but not an updated `wp-settings.php` file. (Do the manual upgrade if you can’t get into wp-admin)

Known Themes with Issues:

- Genesis (minor); Some warnings being displayed in the backend but no impact on functionality. There’s a one-line function that needs to be put in your child themes. The issue only only show up on the theme editor page in single WordPress.
- Elegant Themes (major): Any theme that uses ET’s custom media uploader will have a borked upload modal window (theirs – not WP’s). They’re aware and are looking into it. Please post in ET’s forums for more support.

Please remember, themes not hosted on WordPress.org’s repository are generally not supported here.