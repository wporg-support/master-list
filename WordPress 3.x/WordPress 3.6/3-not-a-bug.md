# NOT A BUG

_You hate the new menus_

Just as many people hated the old ones. Hating the new menus is not a bug.

_TwentyThirteen is a terrible default theme!_

It’s just a theme. If you don’t like it, don’t use it. We know not everyone will like it, and that’s okay. That means that things like ‘The video title is UNDER my video!’ is not a bug, it’s a design choice.

_I thought Post Formats were a big thing! Where’d they go?_

Much like the Dashboard reskin, the [Post Formats UI was removed](http://make.wordpress.org/core/2013/05/29/post-formats-ui-is-exiting-core-will-live-as-a-plugin/). They just weren’t holding up the way everyone wanted them to.

_Two people can’t edit the same post!_

Not a bug. This is intentional. Going forward we’ll want a better filter to let people turn it off though, so keep tabs on [trac ticket 24551](http://core.trac.wordpress.org/ticket/24551) is open. For now, you can use this filter to warn people, but not prevent editing:

```
add_filter( 'show_post_locked_dialog', '__return_false' );
```

(Props Nacin for the correction)