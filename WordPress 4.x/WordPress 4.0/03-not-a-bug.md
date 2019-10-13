# NOT A BUG

_**My layout is all weird on the Dashboard**_

Flush your cache. If you’re using server caches, or a plugin, flush them too, especially Memcached/APC stuff. They can be sticky.

_**The Plugin Update popup box (modal) looks weird and doesn’t show up properly**_

Again, flush your cache. Browser caches sure can be stubborn things sometimes. The problem here is that you’re still seeing the “old” CSS code. Flushing the browser cache and restarting the browser *will* fix this. We promise. 🙂

_**I have a plugin that adds options to the media library and now it’s not working! (also: What happened to the media library!?!)**_

The Media Library defaults to a new, grid, view. This means if you’re using a plugin like the [EWWW Image Optimizer](https://wordpress.org/plugins/ewww-image-optimizer/) that adds in more information, the content may not be visible on the main library view. This is not a bug. The decision was made to make the grid view very simple and basic, allowing you to click on the image to get more information. As time goes by, more plugins will customize that view, but for now you may need to toggle to the LIST view to see it.

At the top-left of the Media toolbar is a button to switch back to the old list view. When switched to the old list view, the button to switch back to the grid view moves to the right.

_**The post/page editor is ‘weird’**_

The post/page editor now auto-expands as you type (it’s a bit more complex than that, but that’s the basic). Previously, the editor had its own scroll bar. This means that if you write a huge post, you need to scroll all the way up to return to the Publish button, categories, tags, etc.

Work-around: Click in the editor and cmd/ctrl-up/down to move to top/bottom of editor content quickly. Click out of the editor and cmd/ctrl-up/down to move to top/bottom of the whole page.

When the editor is larger than the fold, it cannot be scrolled up by highlighting text, due to how the editor toolbar follows the primary scroll.

Work-around: Highlight and scroll outside of the editor window to move the primary scroll instead.

_**The theme customizer moved my options around**_

They changed the default priority for Customizer sections to 160 from 10, which means more ‘priority’ was given to WP defaults vs plugins. It’s okay.

_**My admin panel is now in a different language!**_

If you have tried a different language in the past, WordPress might have saved that in an option and now is using that to display the admin screen in that language. Go to the Settings->General panel (you may need to translate a bit for this) and scroll to the bottom. There is an option named “Site Language” here. See what it is set to. Change it to what you prefer and click the red Save Settings button.