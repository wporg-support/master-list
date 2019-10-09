# TINYMCE/VISUAL EDITOR PROBLEMS?
If you’re using FireFox, upgrade. There ARE issues with FF 3 and TinyMCE (which powers WP’s visual editor).

Some plugins (like TinyMCE Advanced, Rich Category Editor and WP-Stats Dashboard) can also cause this.

Some people have reported that adding this to their wp-config.php corrects the issue:
```
define('CONCATENATE_SCRIPTS', false );
```

As for link info not auto-completing, the devs are aware and are looking into this. No fix yet.

Also remember: switching between editors is the second fastest way to drive you batty 🙂 Don’t jump between visual and HTML editors, that has NEVER been a good idea.