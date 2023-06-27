# CU Boulder Drupal 10 Install Profile

All notable changes to this project will be documented in this file.

Repo : [GitHub Repository](https://github.com/CuBoulder/tiamat10-profile)

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

- ### Shortcode and Migration filters
  Added shortcodes and migration filters to the D10 profile
---

- ### Adds CK Button to D10 profile
  Adds CK Button to D10 profile
---

- ### Adds Google Maps support in Map CKEditor plugin
  This update adds support for Google Maps embeds via an embed code taken from Google Maps.
  
  CuBoulder/tiamat-theme#258
  
  CuBoulder/ucb_ckeditor_plugins#14
  
  Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/16), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/49)
---

- ### Adds Map plugin for embedding Campus Maps
  This update adds the Map plugin to CKEditor, which allows a content editor to provide a link shared from the [CU Boulder Campus Map](https://www.colorado.edu/map/) and embeds a map widget on a page. Just as in the [CKEditor 4 Shortcode](https://websupport.colorado.edu/article/425-campus-map-shortcode) there are three size options to choose from for the widget. The Map plugin outputs web component-like syntax for easier migration and future changes (see `README.md` for the schemas). CuBoulder/ucb_ckeditor_plugins#13
  
  CuBoulder/tiamat-theme#258
  
  Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/15), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/48)
---

- ### Adds a global "Related articles" configuration form to CU Boulder Site Settings
  This update adds a "Related articles" configuration form to CU Boulder Site Settings, accessible via the menu or `/admin/config/cu-boulder/related-articles`. Here users with permission can exclude articles with specific categories or tags from appearing in "related articles" sections. CuBoulder/ucb_site_configuration#22
  
  This update also fixes a bug which caused warnings to appear when configuring a third-party service. CuBoulder/ucb_site_configuration#21
  
  Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/23), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/47)
---

- ### Adds `CHANGELOG.md`, `README.md`, and workflows to `tiamat10-profile`
  Resolves CuBoulder/tiamat10-profile#5 and adds a `README.md` file.
---
