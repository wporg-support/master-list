# REPORTED OOPSIES

If you’re getting weird 502’s and/or half missing general settings screen, then your server has an old version of libssh, and is using ssh for filesystem connections. On the general-settings screen, 4.1 checks the filesystem to see if it is writable by normal means so it knows whether or not to display all available languages, which are now auto-installed/updated.