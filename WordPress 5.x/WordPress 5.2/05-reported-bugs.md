# Reported bugs

Bugs that have been reported against this release of WordPress, with links to tickets for further followup will be listed here.

- **I am unable to update themes** – Some systems may have some trouble with a new file introduced with WordPress 5.2. If possible, try increasing the “Max Execution time” option on your server (or ask your host). More details will be available in [ticket #47186](https://core.trac.wordpress.org/ticket/47186).
- **After a login, the logout hangs or results in an error message**. This is a bug and will be fixed in 5.2.4. See https://core.trac.wordpress.org/ticket/47980
- **Metaboxes overlap on the edit page**. A change in Chrome 77 causes metaboxes to overlap when editing using the block editor. This will be addressed in the next WP update, maybe in a Chrome update, and is fixed in the latest version of Gutenberg, available as a plugin. There’s also a CSS workaround. See https://github.com/WordPress/gutenberg/issues/17406 for details.