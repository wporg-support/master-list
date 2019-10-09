# NOT A BUG

_My layout is all weird on the Dashboard_

Flush your cache. If you’re using server caches, or a plugin, flush them too, especially Memcached/APC stuff. They can be sticky. This includes Cloudflare and Pagespeed and Varnish. Anything that caches.

_I’ve upgraded and the posts are not styled correctly_

Check if you are running `mod_pagespeed` and if you are try disabling it to see if your posts render correctly.

_I’m on 4.4 but I have no JSON Endpoints!_

You have to install the [Rest API plugin](https://wordpress.org/plugins/rest-api/) to actually activate the endpoints.

_Warning: An unexpected error occurred. Something may be wrong with WordPress.org or this server’s configuration._

Despite how it sounds, this typically means that openssl on your server is out of date, unless of course WordPress.org is actually offline. You’ll need to ask your hosting provider upgrade openssl on the server to the latest release (currently 1.0.2e).

_Why didn’t I get Twenty Sixteen?_

Despite WordPress 4.4 containing a new default theme, no themes are installed by WordPress updates, this is intentional. If you were already using WordPress, you’ll need to install Twenty Sixteen from Appearance -> Themes -> Add New in your Dashboard just like any other theme. Twenty Sixteen is included with fresh installations of WordPress 4.4.

_The Comment Field is now above the other fields!_

This is an intentional design decision. By encouraging readers to fill out their comment before their details, the developers hope to increase engagement. The [Reverse Comment Textarea](https://wordpress.org/plugins/reverse-comment-textarea/) plugin will put it back to where it used to be.