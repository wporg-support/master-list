# Reported bugs

Bugs that have been reported against this release of WordPress, with links to tickets for further followup will be listed here.

As WordPress 5.0 is a special release, some known issues have been pre-emptively ticketed, and can be seen in the [WordPress 5.0.2 milestone](https://github.com/WordPress/gutenberg/milestone/83) and [WordPress 5.0.x milestone](https://github.com/WordPress/gutenberg/milestone/74) respectively.

\* 5.0 does not recognize the date format `l j F Y` – This appears to be a translation issue and should be corrected per-language pack.

\* CSV files fail to upload properly in 5.0.1 – This is due to a security patch to validate CSV filetypes. The files are saved as `text/plain` instead of `text/csv` See [Trac 45615](* CSV files fail to upload properly in 5.0.1 – This is due to a security patch to validate CSV filetypes. The files are saved as text/plain instead of text/csv See [Trac 45615 for details.) for details.