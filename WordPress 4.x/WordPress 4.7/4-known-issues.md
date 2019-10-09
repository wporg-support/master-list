# Known Issues

- Paginated comment links are wrong This is a known issue and is being managed in [Trac ticket #39280](https://core.trac.wordpress.org/ticket/39280) (fixed in 4.7.1)
- RSS feeds have incorrect dates when using alternate languages This is a known issue and is being managed in [Trac ticket #39141](https://core.trac.wordpress.org/ticket/39141) (fixed in 4.7.1)
- Uploading files fails for certain extensions, including .docx, .pptx, .mp3. [Trac ticket #39550](https://core.trac.wordpress.org/ticket/39550) For now, use the [Disable Real MIME Check plugin](https://wordpress.org/plugins/disable-real-mime-check/) and remove it as soon as 4.7.3 is released. (fixed in 4.7.3)
- MP3 uploads are split into two files: an MP3 with no cover image, and a corrupt JPG. [Trac ticket #40075](https://core.trac.wordpress.org/ticket/40075) For now, use [Correct Audio/Video Uploads plugin](https://wordpress.org/plugins/correct-audio-video-uploads/) and remove it as soon as 4.7.4 is released. (fixed in 4.7.4)
- When uploading a file, the “Select Files” button will not work under some Chrome configurations. [Trac ticket #40207](https://core.trac.wordpress.org/ticket/40207)