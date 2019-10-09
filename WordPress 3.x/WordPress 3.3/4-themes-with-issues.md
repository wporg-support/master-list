# THEMES WITH ISSUES

Background images not showing

Open `header.php` and locate your `<body>` tag. Change this value to `<body <?php body_class(''); ?>>`

_WooThemes_ framework breaks the upload/insert media link. Per their site, [refreshing your cache will fix this](http://www.woothemes.com/2011/12/wordpress-3-3-is-here/) (props Drew!)

_Atuhualpa_ has some issues with plugins that use the updated jQuery (reported Dec 10th).