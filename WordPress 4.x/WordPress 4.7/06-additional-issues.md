# Additional issue affecting older WordPress releases only

Since WordPress 3.7 came out, WordPress has had auto-update functionality. While the only supported release of WordPress is the latest version, WordPress has used this ability to push automatic security-fix-only releases to older versions of WordPress. These versions only have security fixes applied to them, and no additional functionality.

The latest release of WordPress 4.7.3 was released at the same time as security fixes for every major version backported back to 3.7. Unfortunately, one of those security fixes accidentally relied on a function that was not introduced until WordPress 4.4.

In these WordPress versions, uploading a video or audio file to the media system will result in an “undefined function” error.

- 3.7.19
- 3.8.19
- 3.9.17
- 4.0.16
- 4.1.16
- 4.2.13
- 4.3.9

At this time, the recommended fix is to upgrade to the latest version of WordPress: 4.7.3. Any versions above 4.4 will not have the error, however only the most recent version of WordPress is actually supported.

More information about this issue can be found here:
https://core.trac.wordpress.org/ticket/40085