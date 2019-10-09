# Core Changes

In addition to new features highlighted in [the release post](https://wordpress.org/news/2016/04/coleman/):

**Updated libraries**: We updated jquery, backbone, and a couple other libraries. This may cause your browsers to render oddly. Please remember to flush your cache (browser and website/server). If you’re using Cloudflare, you may need to kick it.

**REST API**: There was a breaking change in the REST API that could potentially break plugins that use it. If you’re not using a plugin to connect with the API, don’t worry. If you are, [check out the Core Post on the subject](https://make.wordpress.org/core/2016/04/06/rest-api-slashed-data-in-wordpress-4-4-and-4-5/).