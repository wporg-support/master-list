# jQuery 1.12 problems

WordPress includes the latest version of jQuery 1.12, which was released back in January: https://blog.jquery.com/2016/01/08/jquery-2-2-and-1-12-released/

It has been discovered that old versions of jQuery worked with an incorrect syntax. That bug was one amongst many bugs fixed in jQuery 1.12. The symptom of this problem is the following message (or something very similar) in the Javascript console when viewing the site in a browser:

> Uncaught Error: Syntax error, unrecognized expression: a[href*=#]:not([href=#])

This is a bit of code that is in somewhat common usage. The problem is that it is incorrect. The link location (hash marks, #, in this case) should be quoted: `a[href*="#"]:not([href="#"])`

Another example would be `a[href=#scroll-to-top]` which, when written correctly, should be `a[href="#scroll-to-top"]`

This can happen in other ways too, this is just one commonplace example. The signs that distinguish this problem are the href and the hash mark (#).

So, what a lot of people are finding out now is that a whole lot of Javascript code out there was doing-it-wrong all this time, and they never noticed because jQuery incorrectly worked with that particular style of broken code. Once WordPress upgraded, and people got the new jQuery, people are now seeing those bugs in their own code.

All that broken Javascript code will need to be fixed. Fortunately, it’s a pretty simple fix, but in the meantime, it’s still broken.

The best advice we can give you is to update all your plugins and themes to the latest versions by their vendors. Plugin and theme authors should be looking to the JS libraries they use for fixes, and including those newer versions of the affected libraries in their code.