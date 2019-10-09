If the TinyMCE fullscreen button is missing, check to see if the site
is still using the pre-2.7 WordPress Automatic Upgrade plugin.
Upgrading with that causes an incomplete (but oddly mostly working)
upgrade.

To fix the problem:

1. Deactivate (and preferably remove) that plugin.
2. Go to the Dashboard->Updates option in the menu.
3. On this new page, select to Re-install WordPress 3.2.1. It’ll spin
a minute and redownload WordPress and install it over itself properly,
fixing any missing or broken files.
4. Clear your browser cache. Your browser will have a copy of the bad
Javascript files in memory, and until you clear them out, it won’t try
to load them from the site again.
5. Done. The full screen button is between the spell check button and
the “kitchen sink” button.