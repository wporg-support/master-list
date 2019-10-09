# TRANSLATION ISSUES

_**NOTE**: This applies to all language packs that were incorrectly pushed out such as nl_NL and en_GB. Once the updated language pack is updated (fixed) then roll back to the current version (3.9.1 as of this edited post) and the issue should be resolved._

If your WordPress version is showing “4.0-alpha” rather than “3.9” for a non US English install this is due to an incorrect localization build for your language.

Other than the incorrect version number there are no other code differences between the versions and include the correct 3.9 translations.

This can cause plugins to display compatibility notices “Warning: This plugin has not been tested with your current version of WordPress”

\* nl_NL has been updated now, though previously it was serving up the wrong revision of WordPress (4.0-alpha), even though the data was correct (3.9)

\* is_IS has not been updated at this stage and is currently serving up the wrong revision of WordPress (4.0-alpha), even though the data is correct (3.9).

Details to resolve the issue can be found [here](https://wordpress.org/support/topic/updat-wp-39-installed-40-alpha?replies=21#post-5470519) once the localization package has been updated.