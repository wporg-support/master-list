**My Virus Scanner tells me WordPress has a Trojan!**

We have confirmed this issue as a **FALSE POSITIVE**.

There is no trojan in WordPress.

Several different virus scanning engines are reporting this false positive:

https://www.virustotal.com/en/file/fda251d8108aa422845c828e5ecc45ad964a45428d6d6d115dfa817131bf2ba7/analysis/

Once again, to confirm, **there is no malware in this file**, despite what the scanners are saying.

The utils.min.js file is a core WordPress file. It is a minified version of the utils.js file in the WordPress core. All that the file does is to do some of the cookie work for the WordPress admin interface.

Minification is an automated process we use to build “smaller” versions of the Javascript files, of which the WordPress core has a lot. These minified files let your site load faster than if we used the originals. However, minification can also make files obscure and hard to read.

Virus scanners don’t actually look for viruses, they look for “signatures”. Sometimes, they put in signatures into the scanning engines that accidentally detect things that are not really there.

Here is the original file:
https://core.svn.wordpress.org/tags/4.4/wp-includes/js/utils.js

Here is the minified version of that file:
https://core.svn.wordpress.org/tags/4.4/wp-includes/js/utils.min.js

Again, this is a **FALSE POSITIVE**. There is no virus or trojan in the WordPress code.

**Update**: Different anti-virus software may react to this in different ways. So far, we have seen everything from the warning above to whole sections of the Dashboard failing to work, all resolved by simply deactivating the anti-virus software or whitelisting the site.

**Update 2**: Bitdefender and F-Secure have both released updates to fix this.