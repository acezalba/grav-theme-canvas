# v2.0.0
## 04/21/2023

1. [](#new)
	* BREAKING - restructured blueprint system to improve settings portability. Old settings from v1 are no longer supported due to renamed blueprint variables. See `blueprints.yaml` and `canvas.yaml` for the new variable system. All themes that use `canvas` as a starter are recommended  to place all page-level blueprint schemas in `default.yaml` and let the partials and theme templates handle if they must access the values in `default.yaml` This unless you really need to lock a set of settings to a specific template.
	* Depreciated template alias files and transferred alias handling to theme logic. This is to declutter the template list in the admin page settings. See `partials/base.html.twig` for the alias lists. If you explicitly want a template alias to appear in the page settings, you must create a new template file that embeds the official template it stands for and register it in the alias lists in `partials/base.html.twig`.
	* Fixed pageflip to only appear if the parent page has a `content.items` explicitly defined.

# v1.0.4
## 01/27/2023

1. [](#bugfix)
	* Bugfix for url of user-uploaded favicon.

# v1.0.3
## 01/24/2023

1. [](#bugfix)
	* Continued fix for breadcrumb css overrides.

# v1.0.2
## 01/24/2023

1. [](#bugfix)
	* Fixed missing breadcrumb css overrides.

# v1.0.1
## 01/24/2023

1. [](#bugfix)
	* Fixed missplaced demo pages.


# v1.0.0
## 01/24/2023

1. [](#new)
	* Added demo pages.
2. [](#bugfix)
	* Fixed url generation for per site custom preview page.
3. [](#improved)
	* Improved `default` and `item` with pageflip urls when they are children of page listings.

# v0.9.0
## 01/24/2023

1. [](#new)
	* Added support for `breadcrumbs` and `pagination` plugin

# v0.8.0
## 01/23/2023

1. [](#new)
	* Added basic support for the `form` plugin
2. [](#bugfix)
	* Fixed `item` template behavior
	* Migrated `item` blueprints to `default` for aliased templates.
3. [](#improved)
	* Improved handling of `modular` pages.

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