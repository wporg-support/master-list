# CHANGES THAT MAY IMPACT YOU

- Masonry Script Updates – Some themes may be [affected by the updated script](http://make.wordpress.org/core/2014/03/27/masonry-in-wordpress-3-9/).
- ‘wpdialogs’ is no longer used by TinyMCE in core – Plugins that rely on it, but do not enqueue it, will need to. There is a warning that will appear in the JavaScript console (which you can debug using the instructions you’ve provided above) if you attempt to use it, and it’s not enqueued.
- If you preview other themes in the customizer, you may lose your widgets. See https://core.trac.wordpress.org/ticket/27897 for details.

**OPEN ISSUES**

The following issues are open trac tickets that are being reviewed and researched. If you have information to add, please do so in trac. Your forum login will let you log in them 🙂 Also once logged in, you can press the ‘watch ticket’ button near the bottom to monitor the ticket.

- [Multisite (#27866)](https://core.trac.wordpress.org/ticket/27866) – SubDirectory installs with uppercase letters in the path will break in 3.9
- [Widgets lost after previewing theme (#27897)](https://core.trac.wordpress.org/ticket/27897) – Changing widgets in the new customizer causes in missing widgets on your live site in some cases.
- [Pasting Tables from Excel/Word is broken (#27909)](https://core.trac.wordpress.org/ticket/27909) – It strips all HTML and, if edited, breaks older posts too.