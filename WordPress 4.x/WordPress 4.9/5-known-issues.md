# Known issues

- Saving posts or pages is not possible in all browsers when using Visual Composer version 5.4.2 or older.

**Plugins with known issues**

- [Contact Form by BestWebSoft](https://wordpress.org/plugins/contact-form-plugin/) will cause the plugin/theme editors to time out and not save your changes. Workaround: Disable this plugin to use the plugin or theme editors.

**mySQLi now default**

- As of 4.9.2, WordPress now uses the mySQLi extension by default. If you have plugins or older code that uses the mysql_* functions directly, these may cease to function. Update your plugins to the latest version, or find alternative plugins.