# Failed to load content css

This issue keeps popping up for users after the 4.8 update, so here’s a more in-depth process of what is happening.

The error means that the editor window was unable to load one or more resources, generally added using the `editor_styles` function, this is primarily added by your theme, but can also be implemented by plugins (if you would like to identify the exact cause of it, please follow the regular troubleshooting steps outlined in the first post of this thread).

This issue can have many root causes, I’ll run through some of them, so you know what you are looking for, or what to inform your theme developer about:

- The style file does not exist at all
- The style file uses one or more `@import()` calls to include files, but the path is wrong
- Your site is using SSL (your URL starts with `https://`), but the resources being loaded are trying to use un-encrypted `http://` links
- The URL being included is an external one, and is incorrect. So far primarily seen with Google Fonts, where a `%2C` is added to the end of the link (this is considered a comma, and the link is invalid from Googles point of view if it ends like this)

All of these situations, and probably some other scenarios we’ve not outlined, cause the warning to show up. What is important to take note of here is that this is just that, a **warning**, it will not affect the performance of your website, it just means the text editor window won’t preview what it will look like as accurately as it could.

This is not a bug in WordPress 4.8, but rather a warning introduced to help you get the best possible editor experience, but unfortunately it is up to the theme and plugin developers to implement the features correctly.