# Known Issues

- When using the code formatting shortcut a race condition (i.e. things happening at the same time) may occur that prevents the text from converting as intended. (See [ticket #36459](https://core.trac.wordpress.org/ticket/36459))
- Image uploads may fail on servers with an older version of Imagick. (See [Trac ticket #36534](https://core.trac.wordpress.org/ticket/36534)) Note: while a fix for WordPress is in progress, updating Imagick on the server is also a solution.
- Some sites may experience their browser stating they have an infinite redirect loop on the front page of their site. – Go into `Settings > General` in the admin dashboard and make sure the URLs there are all lower-case (See [Trac ticket #21602](https://core.trac.wordpress.org/ticket/21602))
- The new inline link editor fails in Firefox and Chrome after Advanced Options is used once. (See [Trac ticket #36732](https://core.trac.wordpress.org/ticket/36732))
- The bundled Twenty Eleven theme has some styling issues for pages with sidebars (See [Trac ticket #36510](https://core.trac.wordpress.org/ticket/36510)). **Fixed in WordPress 4.5.1**