# NOT A BUG

_**My layout is all weird on the Dashboard**_

Flush your cache. If you’re using server caches, or a plugin, flush them too, especially Memcached/APC stuff. They can be sticky.

_**I’ve upgraded and the posts are not styled correctly**_

Check if you are running `mod_pagespeed` and if you are try disabling it to see if your posts render correctly.

_**The title attribute is missing from my ‘Insert Link’ button when I create posts/pages.**_

This was specifically removed – read [otto’s answer](https://wordpress.org/support/topic/insertedit-link-missing-title-field?replies=50&message=closed#post-6868636)