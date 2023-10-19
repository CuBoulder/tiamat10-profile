# CU Boulder Drupal 10 Install Profile

All notable changes to this project will be documented in this file.

Repo : [GitHub Repository](https://github.com/CuBoulder/tiamat10-profile)

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

- ### Adds "Created" column to content administration page
  Resolves CuBoulder/tiamat-theme#505
---

- ### Sets site default email address in the profile
  This update:
  - Sets the site default email address in the profile at install time. CuBoulder/tiamat-theme#500
  - Changes "D9" to "D10" in the Drupal module description.
---

- ### Update field.field.media.image.field_media_image_caption.yml
  Actual placement for this caption item.
  
  Closes #31 
---

- ### Adds home page setting to CU Boulder site settings
  This update to CU Boulder Site Configuration:
  - Adds a new home page setting to CU Boulder site settings. CuBoulder/tiamat-theme#506
  - Adds a new `edit ucb site pages` permission:
    - Architect, Developer, and Site Manager have been given this new permission. 
    - While "Pages" could eventually be split off into its own tab, the settings are found under "General", at least for now. The existing settings in "General" still require `edit ucb site general` to access.
  - Cleans up PHP files in CU Boulder Site Configuration according to Drupal coding standards. Full compliance has not yet been achieved. CuBoulder/ucb_site_configuration#27
  
  Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/28)
---

- ### Fixes UCB Person Page custom modules
  Adds the fixed versions of `UCB Person Title` and `UCB Article Author` to template and profile. Allows First and Last Name fields to create a Person Page title, getting rid of the need to enter a title for these pages. Also automatically creates a Byline taxonomy for newly created Person Pages, for use in the Byline field. 
  
  Includes:
  
  - `tiamat10-project-template` => https://github.com/CuBoulder/tiamat10-project-template/pull/15 (`issue/ucb_person_title/2`)
  -  `tiamat-profile` => https://github.com/CuBoulder/tiamat10-profile/pull/28 (`issue/ucb_person_title/2`)
  -  `ucb_person_title` => https://github.com/CuBoulder/ucb_person_title/pull/4 (`issue/2`)
  -  `ucb_article_author` => https://github.com/CuBoulder/ucb_article_author/pull/2 (`issue/1`)
  
  Resolves https://github.com/CuBoulder/ucb_article_author/issues/1, Resolves https://github.com/CuBoulder/ucb_person_title/issues/2
---

- ### Installs and enables CKEditor 5 Icons
  Installs and enables the [CKEditor 5 Icons](https://www.drupal.org/project/ckeditor5_icons) contrib module and the Icon plugin.
  
  Resolves CuBoulder/tiamat-theme#372
---

- ### Refactoring Installation of CU Default Content
  Resolves CuBoulder/tiamat-theme#488
  
---

## [20230918] - 2023-09-18

-   ### Changing permissions for Content Editor
    Adding in Block permissions for the Content Editor role to resolve CuBoulder/tiamat-theme#486

* * *

-   ### Update boulder_profile.info.yml

    Add new global library dependency at install.

    Sister PR: <https://github.com/CuBoulder/ucb_migration_shortcodes/pull/9>
    Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/485>
    Sister PR: <https://github.com/CuBoulder/tiamat10-project-template/pull/12>

* * *

-   ### New: Adds Button Group plugin to CKEditor

    Adds Button Group to CKeditor5 wysiwyg and full html on install

    Resolves <https://github.com/CuBoulder/tiamat-theme/issues/251>

* * *

-   ### Tiamat theme/issue/149
    Closes <https://github.com/CuBoulder/tiamat-theme/issues/149>.
    Adds profile changes for metatag installation

* * *

-   ### taxonomy implementation
    Closes issue tiamat/theme/27.
    Adds the taxonomy views

* * *

-   ### Update block.block.site_contact_info_footer.yml

    Updated where site contact information is displayed by default

    Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/468>

* * *

-   ### Issue/shortcodes/2
    Sister pull request for ucb_migration_shortcodes/issue/2.
    Adds profile changes for shortcodes

* * *

-   ### Adds the "Calendar" CKEditor 5 plugin

    This update adds a "Calendar" item to CKEditor 5, allowing insertion of Google Calendar embeds via an embed code taken from Google Calendar. Equivalent to the `[googlecalendar]` Shortcode in D7 Express.

    CuBoulder/tiamat-theme#256

    Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/25), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/53)

* * *

-   ### Update filter.format.wysiwyg.yml

    Added new shortcodes to profile

    Sister PR: <https://github.com/CuBoulder/ucb_migration_shortcodes/pull/3>

* * *

-   ### Removes "D9" from theme name and the theme, custom entities Composer package names

    CuBoulder/tiamat-theme#435

    Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/452), [tiamat-custom-entities](https://github.com/CuBoulder/tiamat-custom-entities/pull/70), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/52), [tiamat-project-template](https://github.com/CuBoulder/tiamat-project-template/pull/28), [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/8), [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/26)

* * *

-   ### Remove full justification setting for wysiwyg
    Removing the full justification setting option for they WYSIWYG text authoring configuration.  

* * *

-   ### Adding Nicole Waldrip to the default install
    Added new Architect to the base install profile.  

* * *

-   ### Shortcode and Migration filters
    Added shortcodes and migration filters to the D10 profile

* * *

-   ### Adds CK Button to D10 profile
    Adds CK Button to D10 profile

* * *

-   ### Adds Google Maps support in Map CKEditor plugin

    This update adds support for Google Maps embeds via an embed code taken from Google Maps.

    CuBoulder/tiamat-theme#258

    CuBoulder/ucb_ckeditor_plugins#14

    Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/16), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/49)

* * *

-   ### Adds Map plugin for embedding Campus Maps

    This update adds the Map plugin to CKEditor, which allows a content editor to provide a link shared from the [CU Boulder Campus Map](https://www.colorado.edu/map/) and embeds a map widget on a page. Just as in the [CKEditor 4 Shortcode](https://websupport.colorado.edu/article/425-campus-map-shortcode) there are three size options to choose from for the widget. The Map plugin outputs web component-like syntax for easier migration and future changes (see `README.md` for the schemas). CuBoulder/ucb_ckeditor_plugins#13

    CuBoulder/tiamat-theme#258

    Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/15), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/48)

* * *

-   ### Adds a global "Related articles" configuration form to CU Boulder Site Settings

    This update adds a "Related articles" configuration form to CU Boulder Site Settings, accessible via the menu or `/admin/config/cu-boulder/related-articles`. Here users with permission can exclude articles with specific categories or tags from appearing in "related articles" sections. CuBoulder/ucb_site_configuration#22

    This update also fixes a bug which caused warnings to appear when configuring a third-party service. CuBoulder/ucb_site_configuration#21

    Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/23), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/47)

* * *

-   ### Adds `CHANGELOG.md`, `README.md`, and workflows to `tiamat10-profile`
    Resolves CuBoulder/tiamat10-profile#5 and adds a `README.md` file.

* * *

[Unreleased]: https://github.com/CuBoulder/tiamat10-profile/compare/20230918...HEAD

[20230918]: https://github.com/CuBoulder/tiamat10-profile/compare/b18a1906373a01be11ef84f9cb95d6b171aa9eab...20230918
