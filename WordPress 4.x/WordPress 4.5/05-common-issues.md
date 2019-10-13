_**Issues with Plugins**_

- Visual Composer – Please upgrade to 4.11.2+. The compatibility issue was fixed in Version 4.11 on March 10th: https://wpbakery.atlassian.net/wiki/display/VC/Release+Notes
- Custom Facebook Feeds – Breaks JavaScript rendering. Fixed in 2.4.1.1
- Jetpack – Please make sure you’re connected to Jetpack if you use Photon. Not being connected will cause your images to not display. (nb – this is not a Jetpack or 4.5 bug, just something people are noticing right now)
- XpertAccordian – A premium plugin. It’s not working with the editor due to Javascript updates.
- [a3-lazy-load](https://wordpress.org/plugins/a3-lazy-load/) – Causing images not to show
- [HeadSpace2](https://wordpress.org/plugins/headspace2/) – jQuery 1.12 problems as outlined below
- Beaver Builder plugin – Some reports of CSS issues causing media libraries to not work. More info here: https://wordpress.org/support/topic/wp45-jquery-update-and-table-styles-issue

_**Issues with Themes**_

- **Divi**

  **Divi Version 2.7.3 ( updated 04-13-2016 ) fixes the jQuery issue outlined below. Update your theme.**
  
  Exhibits the jQuery problem as described below. The file js/custom.js has the issue on line 706. Adding double quote marks around the hash symbols (#) will fix it.
  
  Change this:
  
  `$( 'a[href*=#]:not([href=#])' ).click( function() {`
  
  To this:
  
  `$( 'a[href*="#"]:not([href="#"])' ).click( function() {`
  
  Alternatively, check with your theme vendor for an update.

- **Other Themes on Themeforest** – Lots of themes from Themeforest are exhibiting this issue. If you have a theme from there, please contact your theme author for an update to fix any instances of the jQuery problem as listed below.

List of known Themeforest themes with the problem:
Exhibit
TheFox

_**Issues Elsewhere**_

- Users with WordPress installed under Plesk may note a Forbidden error quoting wp-tinymce.php. The solution for this is covered on [Plesk’s support site](http://kb.plesk.com/en/127970).