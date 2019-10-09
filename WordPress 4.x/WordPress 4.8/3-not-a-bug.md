# Not a Bug

**The new media widgets don’t work in my theme.**

If your theme hides widgets by default in some way – like in a slide-out panel – then the new audio and video widgets may not be displayed correctly. If you are a theme developer, [here is an example for solving this](https://themes.trac.wordpress.org/browser/coherent/1.0.6/js/coherent.js?rev=77395#L88).

**Text from the updated text widget is going outside the designated area.**

Your theme will need to be updated to work with the new HTML that the editor will wrap content in after the update to 4.8.

**I am getting a “Failed to load content css” warning.**

This warning appears when a editor style isn’t properly set up (for example a child theme trying to include a parent editor style with `@import` with the wrong path). It will have to be fixed by your theme author so that any link to CSS files are correct.

[See the more detailed post below.](https://wordpress.org/support/topic/read-this-first-wordpress-4-8-master-list/#post-9221234)