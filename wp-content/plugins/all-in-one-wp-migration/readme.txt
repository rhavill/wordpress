=== All-in-One WP Migration ===
Contributors: yani.iliev, bangelov, mirkov
Tags: db migration, migration, wordpress migration, db backup, db restore, website backup, website restore, website migration, website deploy, wordpress deploy, db backup, database export, database serialization, database find replace
Requires at least: 3.3
Tested up to: 3.9
Stable tag: 1.7.1
License: GPLv2 or later

All-in-One WP Migration is the only tools that you will ever needs when you need to perform site migration of your WordPress blog.

== Description ==

The plugin allows you to export your database, media files, plugins, and themes.
You can apply unlimited find and replace operations on your database and the plugin will also fix any serialization problems that occur during find/replace operations.

All in One WP Plugin is the first plugin to offer true mobile experience on WordPress versions 3.3 and up.

= Multisite compatible =
* The plugin menu is available for the network administrator only `wp-admin/network/admin.php?page=site-migration-export`

= Works on Windows OS and IIS =
* Tested the plugin on Windows 7 and Windows Server 2012 with the default available IIS
* You will need to make sure that Windows\TEMP folder has write permissions for the IIS user

= memory_limit requirement of only 32MB =
* The plugin handles archiving of files by using 2048 bytes of chunks
* The plugin processes database find/replacement in chunks of 1MB

= Bypass all upload size restriction =
* We use chunks to import your data and that way we bypass any webserver upload size restrictions up to **512MB** - commercial version supports up to **5GB**

= Works with PHP v5.2.17 and above =
* We tested the plugin on a php compiled with the following modules:
`./configure --with-zlib --with-mysql`

= Support for MySQL, PDO, MySQLi =
* No matter what php mysql driver your webserver ships with, we support it

= Support for ZipArchive and PclZIP =
* Your export files are archived using the fast ZipArchive pecl extension. If your server doesn't have it, we fall back to PclZIP which is included in WordPress

= True WordPress v3.3 Support =
* We tested every single WordPress version from `3.3` up to `3.9`

= Coming soon in a commercial version =
* A new, slicker design
* Themes picker - you can select exactly what themes you want to export - start with just theme names or dig deep and select single files
* Media picker - allows you to select what media files you want to export
* Plugins picker - allows you to select what plugins to export as well as to dig deeper and select the exact files to export
* Database picker - select what tables to export
* Custom post type picker - select what post types to export (pages, posts, events, videos etc)
* Post and Page picker - select what posts or pages you would like to include in your data export.
* Users picker - select the users that you want to include in your export

**If you signup for our beta program, you will receive a free license for the commercial version when we release it as well as a few other perks like a free staging platform and access to our super-fast `Opinionated WordPress Hosting`.**
[All in One WP Migration Beta](https://servmask.com/beta "All in One WP Migration")

[youtube http://www.youtube.com/watch?v=5FMzLf9a4Dc]

== Installation ==

1. Upload the `all-in-one-wp-migration` folder to the `/wp-content/plugins/` directory
1. Activate the All in One WP Migration plugin through the 'Plugins' menu in WordPress
1. Configure the plugin by going to the `Site Migration` menu that appears in your admin menu

== Screenshots ==

1. Mobile Export page
2. Mobile Import page
3. Plugin Menu

== Changelog ==
= 1.7.1 =
* Fixed a bug when exporting WordPress plugins directory

= 1.7.0 =
* Added storage layer to avoid permission issues with OS's directory used for temporary storage
* Added additional checks to verify the consistency of the imported archive
* Fixed a bug that caused the database to be exported without data
* Removed unused variables from package.json file

= 1.6.0 =
* Added additional check for directory's permissions
* Added additional check for output buffering when exporting a file
* Fixed a bug when the archive was exported or imported with old version of Zlib library
* Fixed a bug with permalinks and flushing the rules

= 1.5.0 =
* Added support for additional errors and exceptions handling
* Added support for reporting a problem in better and easier way
* Improved support process in ZenDesk system for faster response time
* Fixed typos on the import page. Thanks to Terry Heenan

= 1.4.0 =
* Adding a twitter and facebook share buttons to the sidebar on import and export pages

= 1.3.1 =
* Fixed a bug when the user was unable to import site archive
* Optimize and speed up import process

= 1.3.0 =
* Added support for mysql connection to happen over sockets or TCP
* Added support for Windows OS and fully tested the plugin on IIS
* Added support for limited memory_limit - 1MB - The plugin now requires only 1MB to operate properly
* Added support for multisite
* Use mysql_unbuffered_query instead of mysql_query to overcome any memory problems
* Fixed a deprecated warning for mysql_pconnect when php 5.5 and above is used
* Fixed memory_limit problem with PCLZIP library
* Fixed a bug when the archive is exported with zero size when using PCLZIP
* Fixed a bug when the archive was exported broken on some servers
* Fixed a deprecated usage of preg_replace \e in php v5.5 and above

= 1.2.1 =
* Fixed an issue when HTTP Error was shown on some hosts after import, credit to Michael Simon
* Fixed an issue when exporting databases with different prefix than wp_, credit to najtrox
* Fixed an issue when PDO is avalable but mysql driver for PDO is not, credit to Jaydesain69
* Delete a plugin specific option when uninstalling the plugin (clean after itself)
* Support is done via Zendesk
* Include WP Version and Plugin version in the feedback form

= 1.2.0 =
* Increased upload limit of files from 128MB to 512MB
* Use ZipArchive with fallback to PclZip (a few users notified us that they don’t have ZipArchive enabled on their servers)
* Use PDO with fallback to mysql (a few users notified us that they dont have PDO enabled on their servers, mysql is deprecated as of PHP v5.5 but we are supporting PHP v5.2.17).
* Support for PHP v5.2.17 and WordPress v3.3 and above.
* Fix a bug during export that causes plugins to not be exported on some hosts (the problem that you are experiencing).

= 1.1.0 =
* Importing files using chunks to overcome any webserver upload size restriction
* Fixed a bug where HTTP code error was shown to some users

= 1.0.0 =

* Export database as SQL file
* Export media files
* Export themes files
* Export installed plugins
* Unlimited Find & replaces
* Option to exclude spam comments
* Option to apply find & replace to GUIDs
* Option to exclude post revisions
* Option to exclude tables data
* WordPress multisite support
