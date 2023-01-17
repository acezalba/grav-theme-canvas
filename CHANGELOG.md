# v0.7.2
## 01/17/2023

1. [](#bugfix)
	* Fixed url and description metadata bugs

# v0.7.1
## 01/17/2023

1. [](#bugfix)
	* Used absolute urls for preview images.

# v0.7.0
## 01/17/2023

1. [](#bugfix)
	* Fixed a major bug that caused user preview images to be wiped out on update. Site-level preview images and favicons will now be uploaded to `user/images`.

# v0.6.0
## 01/17/2023

1. [](#new)
	* Added basic support for `feed` and `sitemap` and declared as requirements/dependencies for the theme.
2. [](#improved)
	* Used asset manager for handling of theme css.
	* Added template alias arrays in the theme to improve template-based theme logic

# v0.5.0
## 01/17/2023

1. [](#new)
	* Added compatibility support for `modular` themes. Errors for when modular template is not present is currently unsuppressed. Solution pending.
	* Added module `section` as a compatibility layer. Dumps module content.
2. [](#bugfix)
	* Fixed inline theme rendering
3. [](#improved)
	* Added more default values for theme

# v0.4.1
## 01/11/2023

1. [](#bugfix)
	* Fixed assets not loading caused by url mapping

# v0.4.0
## 01/07/2023

1. [](#bugfix)
	* Fixed preview image bug caused by variable misspelling

# v0.3.0
## 01/06/2023

1. [](#new)
	* Added template aliases `archive` (blog) , `article` (item), `folder` (blog), `index` (blog), `page` (default), and `post` (item), 
2. [](#bugfix)
	* Fixed chronology of the changelog file

# v0.2.1
## 12/19/2022

1. [](#bugfix)
	* Fixed handling of page content in home pages.
	
# v0.2.0
## 12/19/2022

1. [](#bugfix)
	* Fixed handling of page subtitles across templates. Page summary should now be displayed separately with the page content.

# v0.1.1
## 12/18/2022

1. [](#improved)
	* Fixed `CHANGELOG.md` to conform with semantic versioning and tagging
	* Added dates to `CHANGELOG.md`


# v0.1.0
## 12/18/2022

1. [](#new)
	* Changelog started
	* Built the theme.
	* Added support for `default`, `error`, `blog` and `item` templates.
	* Added theme and page configurations.