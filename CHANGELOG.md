# CU Boulder Drupal 10 Install Profile

All notable changes to this project will be documented in this file.

Repo : [GitHub Repository](https://github.com/CuBoulder/tiamat10-profile)

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [20250312] - 2025-03-12

- ### recaptcha settings move

  Move recaptcha settings from `install` to `optional` to avoid key override

  Resolves #269

* * *

## [20250305] - 2025-03-05

- ### Removing Klaro from the base install
  Klaro is in testing on the Sandbox sites but should not be enable in production.  Moving the config for that module from `config/install` to `config/optional` and setting a module dependency so that this config will be added once the module is turned on.  

* * *

## [20250226] - 2025-02-26

- ### Add Klaro (GDPR) Cookie manager

  Profile and installation settings for the new Klaro! module. 

  Devs and Architects have access to the settings options for Klaro
  anonymous and authenticated users all needed permissions to interact with the popup.

  By default klaro is looking for 

  - gtm
  - ga
  - facebook
  - tiktok
  - youtube
  - vimeo

  Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/1607>
  Sister PR: <https://github.com/CuBoulder/tiamat10-project-template/pull/75>

* * *

- ### Webforms: Modify config to defauts to prevent multiple submissions

  This update turns off Ajax and resets the form config back to mostly default, so that forms aren't submitted multiple times. We are currently working on debugging multi-page form blocks which seem to have the most issues. Strongly recommended to try to keep new Webforms limited to Webform Pages or modify existing Form blocks to pages, especially the more complex multi-page forms until more is known about the issue. 

  With this disabled you should also be able to enable Ajax as a per-form setting, which may help issues with complex multi-page forms. 

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/1330>
  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/215>

* * *

## [20250219] - 2025-02-19

- ### #247 Site Manager: role can view/edit/delete other site manager roles

  Allows the Site Manager role to view/edit/delete other Site Managers and administer Site Owners
  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/247>

  Includes:

  - `drush-commands` => <https://github.com/CuBoulder/ucb_drush_commands/pull/3>
  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/253>

* * *

## [20250212] - 2025-02-12

- ### Update boulder_profile.info.yml

  Make `unpublished_404` on when installed

  Resolved #258 

  Sister PR: <https://github.com/CuBoulder/tiamat10-project-template/pull/74>

* * *

- ### Issue/1597
  Updated profile to enable `entity_usage` and `paragraphs_library` modules. 
  This also sets up the permissions needed for the reusable paragraphs.

* * *

## [20250205] - 2025-02-05

- ### Secondary/Footer sidebar menus

  Added the secondary and footer sidebar menus to work like the main navigation and menus that display with the basic page layout

  Resolves #248 

* * *

- ### Adds Trash module and associated permissions

  Gives Site Manager roles and up the ability to restore deleted content

  Includes:

  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/251>
  - `template` => <https://github.com/CuBoulder/tiamat10-project-template/pull/71>

  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/250>

* * *

## [20250115] - 2025-01-15

- ### #244 Site Managers: sitemap permissions to exclude content

  Gives 'Site Managers' the ability to exclude content from the sitemap

  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/244>

* * *

- ### #235 Allows Webform Submission viewer to navigate to Submissions

  Gives the "Webform Submissions Viewer" Role the ability to navigate to the Submissions page via the toolbar. Previously this was only possible via direct link, but this adds the following permissions to allow that route of navigation:

  - 'access administration pages'
  - 'access toolbar'
  - 'access webform overview'
  - 'view the administration theme'

  Webforms will be the only link that shows up in their Toolbar under Structure

  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/235>

* * *

- ### Removing default users that no longer work here.
  Resolves #241 

* * *

## [20241211] - 2024-12-11

- ### Resolve view issues and adds date functionality

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/1429>.
  Theme - > <https://github.com/CuBoulder/tiamat-theme/pull/1470>.

  This also resolves the issue where 2 created views were creating problems and preventing either from loading.

* * *

## [20241204] - 2024-12-04

## [20241122] - 2024-11-22

## [20241120] - 2024-11-20

- ### Updates to SMTP settings
  A boolean value change for the SMTP configuration and there's a new settings.mail configuration file to be added.  

* * *

- ### Fixes missing help link in the admin toolbar

  This update:

  - Adds permission to access help pages to fix missing help link.

  [bug, severity:minor, permissions] Resolves CuBoulder/tiamat10-profile#229

* * *

- ### Adds Newsletter Archive View

  Adds the`Newsletter Archive` view.

  Includes:

  - `theme` => <https://github.com/CuBoulder/tiamat-theme/pull/1476>
  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/231>
  - `custom-entities`  => <https://github.com/CuBoulder/tiamat-custom-entities/pull/192>

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/1391>
  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/1475>

* * *

## [20241113] - 2024-11-13

- ### Clear Floats Block Style
  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/1451>.
  Adds a clear floats block style.

* * *

## [20241030] - 2024-10-30

## [20241023] - 2024-10-23

## [20241017] - 2024-10-17

- ### Updates linter workflow

  Updates the linter workflow to use the new parent workflow in action-collection.

  CuBoulder/action-collection#7

  Sister PR in: All the things

* * *

- ### Adds Aggregator permission to authenticated users
  [bug, severity:moderate] Resolves CuBoulder/tiamat10-profile#219

* * *

- ### Move main gtm container settings

  Move the main gtm container settings from `config/install` to `config/optional` so that additional tags don't get removed on site updates.

  Resolves #218 

* * *

## [20241009] - 2024-10-09

- ### Create developers-sandbox-ci
  new ci workflow

* * *

## [20241002] - 2024-10-02

- ### Update system.performance.yml

  Created a `system.performance.yml` file at the profile's install. 
  Uses the base system file's info but changed max age to `86400` (One day) 
  All other settings should remain default.

  Resolves #210 

* * *

## [20240925] - 2024-09-25

## [20240919] - 2024-09-19

- ### Moves `google_tag.container.GTM-M3DX2QP.65de22067902c7.57590325.yml` to `config/install`
  [change] Resolves CuBoulder/tiamat10-profile#203

* * *

- ### Move block layout files to optional

  Move the block layout files to optional to stop update overrides. 

  The messages, help, and local task files are still in /install as those shouldn't need to be moved.

* * *

## [20240918] - 2024-09-18

- ### Adds permissions for the Faculty Publication block

  [new] This update adds permissions for the Faculty Publications block.

  CuBoulder/tiamat-theme#1146

  Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/1297), [tiamat-custom-entities](https://github.com/CuBoulder/tiamat-custom-entities/pull/172)

* * *

## [20240911] - 2024-09-11

- ### Tag Container Update for Anonymous only tracking
  The change to the optional install file should make it so only anonymous users are being tracked.
  This looks to fix the admin control issues too. 
  The logged in users now see youtube videos loading properly for video reveal/hero blocks. They are still sometimes broken on anonymous users.

* * *

## [20240904] - 2024-09-04

- ### Permissions for Mega Menu
  Closes #194.
  Adds the permissions needed for Mega Menu editing.

* * *

## [20240821] - 2024-08-21

- ### Update filter.format.wysiwyg.yml

  Filter updates to remove "focal point" styles.
  Updated the default to be large to remove an option.

  Sister PR: <https://github.com/CuBoulder/tiamat-custom-entities/pull/163>

  Closes #191 

* * *

- ### Updates Metatag settings

  This update:

  - [bug] Fixes meta tags missing on a site's home page but not other pages.
  - [change] Resolves description meta tag to summary field instead of body field.

  Resolves CuBoulder/tiamat10-profile#189

* * *

- ### Add menu extras module
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/629>.
  Adds the ncessary module for the mega menu.

* * *

- ### Adds CU Boulder Styled Block custom module and updates block styles

  This update:

  - [new] Adds the new CU Boulder Styled Block custom module.
  - [new] Converts the Campus News block to a styled block, adding new style options to match our other blocks. CuBoulder/ucb_campus_news#6 CuBoulder/ucb_campus_news#9
  - [change] Refactors existing styled blocks to all extend the same Twig template with Twig inheritance.
  - [change] Corrects some indentation and other minor code style issues in affected block templates.

  Sister PR in: [ucb_campus_news](https://github.com/CuBoulder/ucb_campus_news/pull/10), [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/1209), [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/55)

* * *

## [20240814] - 2024-08-14

- ### Cleaning up default users
  Removing Nicole from the Architects list and moving Kevin from Dev to Architect by default for new sites.  

* * *

- ### New Image Styles: Colorbox Image Styles

  Adds Colorbox images to editor filters

  ### New Image Styles

  Adds 4 new colorbox image styles: `Colorbox Small` , `Colorbox Small Square`, `Colorbox Small Thumbnail`, `Colorbox Square`. On click, these open up a modal with the full image and caption.

  Includes:

  - `tiamat-theme` => <https://github.com/CuBoulder/tiamat-theme/pull/1205>
  - `tiamat-custom-entities` => <https://github.com/CuBoulder/tiamat-custom-entities/pull/160>
  - `tiamat-profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/185>

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/1174>

* * *

- ### Update webform.settings.yml

  Change default values for webform email and name

  Resolves #183 

* * *

- ### CK Styles: Margin Clear

  Adds a 'Margin Clear' style for headers and paragraphs

  Includes:
  \-`tiamat-profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/182>
  \-`tiamat-theme` => <https://github.com/CuBoulder/tiamat-theme/pull/1201>

  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/152>

* * *

- ### Enabling ucb_drush_commands in the profile
  Enabling new module for Drush commands.  

* * *

## [20240805] - 2024-08-05

- ### Adds new Image Style to Editor Filters

  Includes:

  - `tiamat-custom-entities` => <https://github.com/CuBoulder/tiamat-custom-entities/pull/155>
  - `tiamat-profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/177>

  Resolves <https://github.com/CuBoulder/tiamat-custom-entities/issues/154>

* * *

- ### GTM Consent Update
  Change the consent mode from `true` to `false` to allow for tracking to work correctly. This change is being made in the interim before having a consent module so that tracking works across D10 sites.

* * *

- ### Adds 'Jump Menu' to profile on install

  Resolves <https://github.com/CuBoulder/ucb_ckeditor_plugins/issues/74>

  Includes:

  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/168>
  - `ucb_ckeditor_plugins` => <https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/87>

* * *

- ### Removes shortcodes & updates WYSIWYG settings
  This update:
  - [Remove] Removes shortcodes from the profile. Resolves CuBoulder/tiamat10-profile#171
  - [Bug] Corrects Map plugin filter out of order. Resolves CuBoulder/tiamat10-profile#169
  - [Change] Enables Linkit URL Converter filter. Resolves CuBoulder/tiamat10-profile#165

* * *

## [20240725] - 2024-07-25

- ### Move smtp to config/optional
  Closes #170.
  Adds the smtp file to a new folder config/optional in an attempt to prevent password wiping.

* * *

## [20240719] - 2024-07-19

- ### Issue/155
  Closes #155.
  Adds the column list styles for both ul and ol.

* * *

- ### Google Tag Update

  Updaing the google tag manager code from the Universal Analytics to the newer global tag manager code. This is done in the Tag Manager module.
  Site users can still put their personal codes in the GTM section of site settings.

  Resolve #163 

* * *

## [20240711] - 2024-07-11

- ### Add permission to site manager
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/1097>.
  Adds the bypass node access permission to the site manager role.

* * *

- ### Adds the CKEditor 5 Bootstrap Accordion module

  This update:

  - Adds the [CKEditor 5 Bootstrap Accordion](https://www.drupal.org/project/ckeditor5_bootstrap_accordion) module.
  - Adds the "Accordion" item to the CKEditor 5 toolbar for the WYSIWYG and Full HTML text formats.

  Resolves CuBoulder/tiamat10-profile#160

  Sister PR in: [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/48)

* * *

- ### Add administer blocks permission to site manager
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/1099>.
  Adds the administer blocks permission, as that is layout manager's only permission to the site manager.

* * *

- ### Adds Column plugin to profile

  Adds the new plugin 'Column' to the CKEditor5 toolbar on install

  Includes:

  - `ucb_ckeditor_plugins` => <https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/85>
  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/156>

  Resolves <https://github.com/CuBoulder/ucb_ckeditor_plugins/issues/75>

* * *

- ### Update filter.format.wysiwyg.yml
  Updated the allowed_html to have the new callout class

* * *

- ### Invisible: adds 'visually-hidden' to allowed

  ### Invisible Plugin

  Switches depreciated 'sr-only' class to 'visually-hidden' class, adds to allowed

  Resolves <https://github.com/CuBoulder/ucb_ckeditor_plugins/issues/78>
  Includes:

  - ckeditor_plugins => <https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/79>
  - boulder_profile => <https://github.com/CuBoulder/tiamat10-profile/pull/153>

* * *

- ### Social media menu region removal
  Used in conjunction with <https://github.com/CuBoulder/tiamat-theme/pull/1051>.
  Removes the Social Media Menu Region and moves the Social Media Menu to the Footer Menu.

* * *

- ### Fixes permissions for Social Media Icons block
  Resolves CuBoulder/tiamat10-profile#150

* * *

## [20240612] - 2024-06-12

- ### Adds Rebuild Cache Access contrib module

  This new contrib module adds a "Rebuild Cache" option in the toolbar, accessible to architects and developers. **Use this sparingly and only as a last resort after you've tried everything else, such as clearing local browser caches. A cache rebuild is an administrative action that has temporary negative effects on the performance of the site.**

  Resolves CuBoulder/tiamat10-profile#147

  Sister PR in: [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/47)

* * *

- ### Adds small styles to WYSIWYG editor
  Resolves CuBoulder/tiamat-theme#829.
  Adds the small style for text in 2 forms. There is a block style called Small that wraps it in a `<p>` and a text style called Small Span that wraps it in a `<span>`

* * *

- ### Media Image: Sets Default to use 'Large (1500px, 100% display size)'

  ### Media Image

  - Sets `Default` to use 'Large (1500px, 100% display size)' Image Style

  Resolves <https://github.com/CuBoulder/tiamat10-profile/issues/144>

* * *

## [20240604] - 2024-06-04

- ### Video: adds missing URL field to form

  ### Video

  Previously the video url was missing if you went to upload video media via `Content => Media => Add Media => Video`, resulting in just a title input there. This has been corrected.

  Resolves #141 

* * *

- ### Removing blank password line from smtp configuration
  This may cause issues down the line if it attempts to blank out a set password on update.  Removing that line from the config.  

* * *

- ### Captcha: Adds config and enables on install

  Adds config and enables on install for Captcha v3. Needs site keys for v3.

  Includes:

  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/138>
  - `project-template` => <https://github.com/CuBoulder/tiamat10-project-template/pull/45>

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/617>

* * *

- ### Configures nodes to show up in XML sitemap
  [Change] Resolves CuBoulder/tiamat10-profile#139

* * *

- ### Adding in SMTP config and enabling SAML
  Adding production modules and some config needed for Pantheon in production.  

* * *

- ### Adds `bypass node access` permission to Architect and Content Editor roles
  [Change] This update adds a permission which disables access restrictions on unpublished content as well as any other content access restrictions, to the Architect and Content Editor roles. Resolves CuBoulder/tiamat10-profile#112

* * *

- ### Updates user invite configuration

  [Change] This update changes the login link to an HTML link in invite email messages.

  CuBoulder/ucb_user_invite#8

  Sister PR in: [ucb_user_invite](https://github.com/CuBoulder/ucb_user_invite/pull/9)

* * *

- ### Adds 'View News Feed' permission to Anonymous Users

  Adds the needed permission to allow anonymous users to view news feeds on the Aggregator Block. Previously the RSS feed element portion of the block would not display at all for anonymous users, causing image issues as the image part of the block would be the only part rendered.

  Resolves #129 

* * *

## [20240513] - 2024-05-13

- ### Update filter.format.wysiwyg.yml

  Added `aria-hidden="true"` as acceptable html.
  This is needed for the new update in the ckeditor 5 plugin

  Sister PR: <https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/60>
  Sister PR: <https://github.com/CuBoulder/ucb_migration_shortcodes/pull/20>

* * *

- ### Adds `text-align-center` and `text-align-right` as permitted classes for `<th>` and `<td>` in WYSIWYG fields
  Resolves CuBoulder/tiamat10-profile#116

* * *

- ### Updates allowed file types for the document media type
  Resolves CuBoulder/tiamat10-profile#118

* * *

- ### Adds Anchor to WYSIWYG and Full HTML, removes Devel permissions

  - Adds Anchor to WYSIWYG and Full HTML text editors, CK5 toolbars and allowed elements. 
  - Removes Devel permissions from Architect and Developer. Also removes the 'switch user' permission -- all of which would break `install-site`

  Resolves #121 
  Resolves #120 

  Includes:

  - `tiamat-profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/122>
  - `project-template`=> <https://github.com/CuBoulder/tiamat10-project-template/pull/43>

* * *

- ### Removes the Devel contrib module

  Resolves CuBoulder/tiamat10-profile#108

  Sister PR in: [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/42)

* * *

- ### Update block.block.boulder_base_sidebar_menu.yml

  Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/898>
  Sister PR: <https://github.com/CuBoulder/ucb_bootstrap_layouts/pull/38>
  Sister PR: <https://github.com/CuBoulder/tiamat-custom-entities/pull/135>

  Update for sidebar menu to not be displayed on basic page node types.
  This is so that every other page that isn't a basic page will still get the navigation from the block layout.

* * *

- ### Issue/tiamat theme/804
  Sister pull request to close <https://github.com/CuBoulder/tiamat-theme/issues/804>.
  Adds the necessary profile changes to add wallpaper image style.

* * *

- ### remove how-to from permissions
  Sister request to <https://github.com/CuBoulder/tiamat-custom-entities/pull/134>.
  Removes all necessary permissions for the removal of the how-to pages.

* * *

- ### Form Configuration

  Fixes the following configuration on forms and made config changes requested by Kevin during our Site Accessibility Review:

  - Disable client-side validation for all webforms
  - Display required indicator on all webforms
  - Use Ajax for all webforms by default
  - Adds Antibot to all webforms by default

  These changes and adding custom profile configuration for the default 'Contact' form allow both single and multipage forms to submit on Form Pages and Blocks

  Resolves #110 

* * *

- ### Remove Video Hero Access

  Removed video hero access
  Users are still able to see that the item exists but they are unable to create or edit them.

  Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/808>

* * *

- ### Adds Responsive Preview on install

  Includes:

  - `profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/107>
  - `project-template` => <https://github.com/CuBoulder/tiamat10-project-template/pull/39>

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/720>

* * *

- ### Adds major User Invite settings update, Linkit document matcher

  This update:

  - [New] Enables selection of multiple user roles for an invite. Previously only one role could be selected.
  - [New] Adds role descriptions, which can be edited in settings.
  - [Change] Updates the default user invite custom message to be blank. Resolves CuBoulder/tiamat10-profile#104
  - [Change] Changes the namespace of the CU Boulder User Invite settings.
  - [New] Adds Linkit profile settings to suggest documents. Resolves CuBoulder/tiamat10-profile#97

  CuBoulder/ucb_user_invite#6

  Sister PR in: [ucb_user_invite](https://github.com/CuBoulder/ucb_user_invite/pull/7)

* * *

- ### Block Styles update

  Updated Editor, Filter, and user permissions for Block Styles

  Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/729>
  Sister PR: <https://github.com/CuBoulder/tiamat-custom-entities/pull/106>

* * *

- ### Change paste filter to accept ckeditor values
  Closes #86.
  Removes some of the paste filters to accept ckeditor values. This may have negative consequences on copy-pastes from word and other text editors.

* * *

- ### Removes child menu items from mobile menus
  Displays only the root menu items. Resolves CuBoulder/tiamat10-profile#96

* * *

- ### Update administer content permission

  Adds the administer content permission to all 4 main roles.

  Resolves CuBoulder/tiamat10-profile#59
  Resolves CuBoulder/tiamat10-profile#94

* * *

- ### Adds "Google Tag" contrib module

  Adds [Google Tag](https://www.drupal.org/project/google_tag) contrib module to serve Google Analytics 4 trackers. The settings were copied over to match D7 Express. Only Architects and Developers can configure Google Tag.

  Resolves CuBoulder/tiamat10-profile#90

  Sister PR in: [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/35)

* * *

- ### Deprioritizes the "Aggregator HTML" text format
  The "Aggregator HTML" text format should now show up at the bottom of the list. Resolves CuBoulder/tiamat10-profile#83

* * *

- ### Fixes Articles being duplicated on Taxonomy pages
  Resolves CuBoulder/tiamat10-profile#88

* * *

- ### Updates Webform element settings
  Resolves CuBoulder/tiamat10-profile#81

* * *

- ### Adds "Administer Users by Role" contrib module and associated configuration

  Allows Site Managers to configure users with an equal or lower permission level, including adding or removing roles of an equal or lower permission level.

  Resolves CuBoulder/tiamat10-profile#78

  Sister PR in: [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/33)

* * *

## [20240221] - 2024-02-21

- ### Adds mobile menus! changes

  - Expands all main menu child menu items. (CuBoulder/tiamat-theme#647)

  CuBoulder/tiamat-theme#653

  Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/660)

* * *

- ### Create layout_builder_iframe_modal.settings.yml
  Added missing settings yml for the iframe builder

* * *

- ### Adds sidebar menu block

  CuBoulder/tiamat-theme#633

  Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/650), ~~[ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/45)~~

* * *

- ### Linkit and iframe modal

  Added linkit to the install profile.
  Updated developer permissions to handle linkit and iframe modal

  Includes:

  - tiamat10-project-tempate => <https://github.com/CuBoulder/tiamat10-project-template/pull/32>

* * *

- ### Class Note Enhancements

  Adjusts permissions for Class Notes, adds optional image field. Resolves <https://github.com/CuBoulder/tiamat-theme/issues/622>

  Includes:

  - tiamat-theme => <https://github.com/CuBoulder/tiamat-theme/pull/648>
  - tiamat-profile => <https://github.com/CuBoulder/tiamat10-profile/pull/75>
  - custom-entities => <https://github.com/CuBoulder/tiamat-custom-entities/pull/94>

* * *

- ### profile changes for collections
  Helps close <https://github.com/CuBoulder/tiamat-theme/issues/534>.
  Adds the necessary permissions for collection objects.

* * *

- ### Fixes permissions with FAQ Pages
  Resolves #71 

* * *

- ### Adds User Invite configuration; adds Webform permissions to Site Manager role
  Resolves CuBoulder/tiamat10-profile#60
  Resolves CuBoulder/tiamat10-profile#61
  CuBoulder/tiamat10-profile#65

* * *

- ### Adds + Enables Menu First Child Module on Install

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/637>

  Includes:

  - `express-admin` (issue/tiamat-theme/637) => <https://github.com/CuBoulder/express_admin/pull/4>
  - `tiamat10-profile`(issue/tiamat-theme/637) => <https://github.com/CuBoulder/tiamat10-profile/pull/70>
  - `tiamat10-project template` (issue/tiamat-theme/637) => <https://github.com/CuBoulder/tiamat10-project-template/pull/31>

* * *

- ### Modal module change

  Changing from modal to iframe modal

  Sister PRs:
  <https://github.com/CuBoulder/tiamat-theme/pull/639>
  <https://github.com/CuBoulder/ucb_bootstrap_layouts/pull/23>
  <https://github.com/CuBoulder/tiamat10-project-template/pull/30>

* * *

- ### Switching to Express Admin for the administration theme
  Express Admin administration sub-theme with Claro as the base theme set as the default admin theme.  

* * *

- ### Adds default Shortcuts

  Adds two requested default Shortcuts:

  - Blocks (admin/content/block)
  - Main menu (admin/structure/menu/manage/main)

  Resolves CuBoulder/tiamat10-profile#63

* * *

- ### Claro theme changes
  Changes done for the claro theme move over

* * *

- ### Adds Redirect + Video Hero Unit Permissions

  ### Two Permissions changes:

  - The content creator roles (Architect, Content Editor, Developer, Site Manager) have been given ability to manage redirects.

  - Anotmirrored the permissions of the Hero Unit to the new separate Video Hero Unit. 

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/556>

* * *

- ### Remove 'Categories' taxonomy term + Associated Permissions
  Removing the **_'Categories'_** taxonomy term and permissions associated with it, as all current Content Types and Blocks use the correct taxonomy term **'Category'** for terms and sorting/filtering. There were no references to the deleted **_'Categories'_** term in `ucb_custom_entities` or any other custom modules, such as `Campus News` or `Site Configuration`, only fields with a machine name that included the word 'categories", but this was only in reference to a collection of **'Category'** terms and not the actual _**'Categories'**_ term.
  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/587>

* * *

## [20231212] - 2023-12-12

- ### Updating role permissions
  Updating role permissions to more accurately reflect the needs of our Express roles.  

* * *

- ### CU Boulder Site Configuration 2.6

  This update:

  - Moves all settings from "Pages and Search" into "General". Search settings are now advanced settings.
  - Replaces the "Pages and search" and "Related articles" tabs with a brand new "Content types" tab. All "Related articles" settings have been moved into "Content types".
  - Replaces the `edit ucb pages` and `configure ucb related articles` permissions with a new `edit ucb content types` permission.
  - Moves the People List filter labels and Article date format into "Content types".
  - Moves the GTM account setting into "General" as an advanced setting.

  CuBoulder/ucb_site_configuration#36

  Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/38), [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/576)

* * *

- ### Scheduler Permissions
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/554>.
  Adds scheduler permissions for various roles.

* * *

- ### CU Boulder Site Configuration 2.5.2

  This update:

  - Places "Type" and "Affiliation" under  an "Advanced" section in the "General" settings. This section behaves identically to the one in "Appearance and layout", requiring the same special permission to access.
  - Gives the "Site Manager" role the `edit ucb site general` permission to access the "General" settings.

  Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/34)
  CuBoulder/ucb_site_configuration#33

* * *

- ### Completes in-content menu blocks

  This update completes in-content menu blocks (menu blocks placed outside of a navigation bar, e.g. in a sidebar) by styling them and adding the [Menu Block](https://www.drupal.org/project/menu_block) contrib module for additional options.

  Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/552), [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/25), [ucb_admin_menus](https://github.com/CuBoulder/ucb_admin_menus/pull/13)

  CuBoulder/tiamat-theme#267
  CuBoulder/tiamat-theme#528

* * *

- ### Adding in Scheduler module
  Used for <https://github.com/CuBoulder/tiamat-theme/issues/504>.
  Adds necessary profile changes for the scheduler module implementation.

* * *

- ### paste filter profile change
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/537>.
  Adds profile changes necessary for the paste filter module.

* * *

- ### Updated block permissions
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/536>.
  Adds the content editor permissions to the developer, architect, and site manager roles

* * *

- ### Issue/510

  Profile updates for the new media file changes

  Settings + profile install 

  Sister PR: <https://github.com/CuBoulder/tiamat10-project-template/pull/22>

* * *

- ### Adds search frontend and settings

  This update:

  - Adds a search modal which appears when clicking on the search icon in the top bar.
  - Adds a new "Pages and search" tab to CU Boulder site settings (`/admin/config/cu-boulder/pages`). This tab contains settings accessible to Architect, Developer, and Site Manager:
    - The home page setting (moved from "General").
    - Options to enable site search, all of Colorado.edu search (default), both, or neither.
    - Configuration for the site search label, placeholder, and URL.
  - Renames "Appearance" to "Appearance and layout" and alters the descriptions of menu items.
  - Adds the [Google Programmable Search Engine](https://www.drupal.org/project/google_cse) module, which allows creating custom search pages to use with site search.

  CuBoulder/tiamat-theme#266

  Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/527), [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/29), [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/17)

* * *

- ### Moving simplesamlphp_auth config to optional
  Added dependency to config as well.   

* * *

- ### Remove Tooltip

  Remove the editor and filter information for `tooltip` as it is not needed and out-of-date

  Closes #41 

* * *

- ### Resolves configuration conflict for Image Styles causing issues on the Admin Interface

  Removes conflicting/duplicate `Image Style` configuration from `profile` that already existed in `custom-entities`, which caused the Admin interface to WSOD while trying to update the Image Styles via UI. 

  Includes:

  - `profile` => [`issue/tiamat-theme/524`](https://github.com/CuBoulder/tiamat10-profile/pull/40)
  - `custom-entities` => [`issue/tiamat-theme/524` ](https://github.com/CuBoulder/tiamat-custom-entities/pull/82)

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/524>

* * *

- ### Wide Image Size Adjustment

  Sets the `Wide` image style size to 1500x563px

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/518>

* * *

- ### Issue/36

  Added allowed HTML and wysiwyg button

  Sister PR: <https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/37>

* * *

- ### Content Styles
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/515>.
  Adds the necessary html tags for new styles added in Issue 515

* * *

- ### initial site manager and content editor roles
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/514>.
  Adds the initial site manager and content editor accounts.

* * *

- ### fixed wysiwyg toolbar ordering
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/503>.
  Fixes ordering of the toolbar of the WYSIWYG text editor. The current missing link is the styles tab, as we currently have no styles.

* * *

- ### Profile clean up
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/501>.
  Cleans up the profile.

* * *

- ### Adds "Created" column to content administration page
  Resolves CuBoulder/tiamat-theme#505

* * *

- ### Sets site default email address in the profile
  This update:
  - Sets the site default email address in the profile at install time. CuBoulder/tiamat-theme#500
  - Changes "D9" to "D10" in the Drupal module description.

* * *

- ### Update field.field.media.image.field_media_image_caption.yml

  Actual placement for this caption item.

  Closes #31 

* * *

- ### Adds home page setting to CU Boulder site settings

  This update to CU Boulder Site Configuration:

  - Adds a new home page setting to CU Boulder site settings. CuBoulder/tiamat-theme#506
  - Adds a new `edit ucb site pages` permission:
    - Architect, Developer, and Site Manager have been given this new permission. 
    - While "Pages" could eventually be split off into its own tab, the settings are found under "General", at least for now. The existing settings in "General" still require `edit ucb site general` to access.
  - Cleans up PHP files in CU Boulder Site Configuration according to Drupal coding standards. Full compliance has not yet been achieved. CuBoulder/ucb_site_configuration#27

  Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/28)

* * *

- ### Fixes UCB Person Page custom modules

  Adds the fixed versions of `UCB Person Title` and `UCB Article Author` to template and profile. Allows First and Last Name fields to create a Person Page title, getting rid of the need to enter a title for these pages. Also automatically creates a Byline taxonomy for newly created Person Pages, for use in the Byline field. 

  Includes:

  - `tiamat10-project-template` => <https://github.com/CuBoulder/tiamat10-project-template/pull/15> (`issue/ucb_person_title/2`)
  - `tiamat-profile` => <https://github.com/CuBoulder/tiamat10-profile/pull/28> (`issue/ucb_person_title/2`)
  - `ucb_person_title` => <https://github.com/CuBoulder/ucb_person_title/pull/4> (`issue/2`)
  - `ucb_article_author` => <https://github.com/CuBoulder/ucb_article_author/pull/2> (`issue/1`)

  Resolves <https://github.com/CuBoulder/ucb_article_author/issues/1>, Resolves <https://github.com/CuBoulder/ucb_person_title/issues/2>

* * *

- ### Installs and enables CKEditor 5 Icons

  Installs and enables the [CKEditor 5 Icons](https://www.drupal.org/project/ckeditor5_icons) contrib module and the Icon plugin.

  Resolves CuBoulder/tiamat-theme#372

* * *

- ### Refactoring Installation of CU Default Content
  Resolves CuBoulder/tiamat-theme#488

* * *

## [20230918] - 2023-09-18

- ### Changing permissions for Content Editor
  Adding in Block permissions for the Content Editor role to resolve CuBoulder/tiamat-theme#486

* * *

- ### Update boulder_profile.info.yml

  Add new global library dependency at install.

  Sister PR: <https://github.com/CuBoulder/ucb_migration_shortcodes/pull/9>
  Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/485>
  Sister PR: <https://github.com/CuBoulder/tiamat10-project-template/pull/12>

* * *

- ### New: Adds Button Group plugin to CKEditor

  Adds Button Group to CKeditor5 wysiwyg and full html on install

  Resolves <https://github.com/CuBoulder/tiamat-theme/issues/251>

* * *

- ### Tiamat theme/issue/149
  Closes <https://github.com/CuBoulder/tiamat-theme/issues/149>.
  Adds profile changes for metatag installation

* * *

- ### taxonomy implementation
  Closes issue tiamat/theme/27.
  Adds the taxonomy views

* * *

- ### Update block.block.site_contact_info_footer.yml

  Updated where site contact information is displayed by default

  Sister PR: <https://github.com/CuBoulder/tiamat-theme/pull/468>

* * *

- ### Issue/shortcodes/2
  Sister pull request for ucb_migration_shortcodes/issue/2.
  Adds profile changes for shortcodes

* * *

- ### Adds the "Calendar" CKEditor 5 plugin

  This update adds a "Calendar" item to CKEditor 5, allowing insertion of Google Calendar embeds via an embed code taken from Google Calendar. Equivalent to the `[googlecalendar]` Shortcode in D7 Express.

  CuBoulder/tiamat-theme#256

  Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/25), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/53)

* * *

- ### Update filter.format.wysiwyg.yml

  Added new shortcodes to profile

  Sister PR: <https://github.com/CuBoulder/ucb_migration_shortcodes/pull/3>

* * *

- ### Removes "D9" from theme name and the theme, custom entities Composer package names

  CuBoulder/tiamat-theme#435

  Sister PR in: [tiamat-theme](https://github.com/CuBoulder/tiamat-theme/pull/452), [tiamat-custom-entities](https://github.com/CuBoulder/tiamat-custom-entities/pull/70), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/52), [tiamat-project-template](https://github.com/CuBoulder/tiamat-project-template/pull/28), [tiamat10-project-template](https://github.com/CuBoulder/tiamat10-project-template/pull/8), [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/26)

* * *

- ### Remove full justification setting for wysiwyg
  Removing the full justification setting option for they WYSIWYG text authoring configuration.  

* * *

- ### Adding Nicole Waldrip to the default install
  Added new Architect to the base install profile.  

* * *

- ### Shortcode and Migration filters
  Added shortcodes and migration filters to the D10 profile

* * *

- ### Adds CK Button to D10 profile
  Adds CK Button to D10 profile

* * *

- ### Adds Google Maps support in Map CKEditor plugin

  This update adds support for Google Maps embeds via an embed code taken from Google Maps.

  CuBoulder/tiamat-theme#258

  CuBoulder/ucb_ckeditor_plugins#14

  Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/16), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/49)

* * *

- ### Adds Map plugin for embedding Campus Maps

  This update adds the Map plugin to CKEditor, which allows a content editor to provide a link shared from the [CU Boulder Campus Map](https://www.colorado.edu/map/) and embeds a map widget on a page. Just as in the [CKEditor 4 Shortcode](https://websupport.colorado.edu/article/425-campus-map-shortcode) there are three size options to choose from for the widget. The Map plugin outputs web component-like syntax for easier migration and future changes (see `README.md` for the schemas). CuBoulder/ucb_ckeditor_plugins#13

  CuBoulder/tiamat-theme#258

  Sister PR in: [ucb_ckeditor_plugins](https://github.com/CuBoulder/ucb_ckeditor_plugins/pull/15), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/48)

* * *

- ### Adds a global "Related articles" configuration form to CU Boulder Site Settings

  This update adds a "Related articles" configuration form to CU Boulder Site Settings, accessible via the menu or `/admin/config/cu-boulder/related-articles`. Here users with permission can exclude articles with specific categories or tags from appearing in "related articles" sections. CuBoulder/ucb_site_configuration#22

  This update also fixes a bug which caused warnings to appear when configuring a third-party service. CuBoulder/ucb_site_configuration#21

  Sister PR in: [ucb_site_configuration](https://github.com/CuBoulder/ucb_site_configuration/pull/23), [tiamat-profile](https://github.com/CuBoulder/tiamat-profile/pull/47)

* * *

- ### Adds `CHANGELOG.md`, `README.md`, and workflows to `tiamat10-profile`
  Resolves CuBoulder/tiamat10-profile#5 and adds a `README.md` file.

* * *

[unreleased]: https://github.com/CuBoulder/tiamat10-profile/compare/20250312...HEAD
[20250312]: https://github.com/CuBoulder/tiamat10-profile/compare/20250305...20250312
[20250305]: https://github.com/CuBoulder/tiamat10-profile/compare/20250226...20250305
[20250226]: https://github.com/CuBoulder/tiamat10-profile/compare/20250219...20250226
[20250219]: https://github.com/CuBoulder/tiamat10-profile/compare/20250212...20250219
[20250212]: https://github.com/CuBoulder/tiamat10-profile/compare/20250205...20250212
[20250205]: https://github.com/CuBoulder/tiamat10-profile/compare/20250115...20250205
[20250115]: https://github.com/CuBoulder/tiamat10-profile/compare/20241211...20250115
[20241211]: https://github.com/CuBoulder/tiamat10-profile/compare/20241204...20241211
[20241204]: https://github.com/CuBoulder/tiamat10-profile/compare/20241122...20241204
[20241122]: https://github.com/CuBoulder/tiamat10-profile/compare/20241120...20241122
[20241120]: https://github.com/CuBoulder/tiamat10-profile/compare/20241113...20241120
[20241113]: https://github.com/CuBoulder/tiamat10-profile/compare/20241030...20241113
[20241030]: https://github.com/CuBoulder/tiamat10-profile/compare/20241023...20241030
[20241023]: https://github.com/CuBoulder/tiamat10-profile/compare/20241017...20241023
[20241017]: https://github.com/CuBoulder/tiamat10-profile/compare/20241009...20241017
[20241009]: https://github.com/CuBoulder/tiamat10-profile/compare/20241002...20241009
[20241002]: https://github.com/CuBoulder/tiamat10-profile/compare/20240925...20241002
[20240925]: https://github.com/CuBoulder/tiamat10-profile/compare/20240919...20240925
[20240919]: https://github.com/CuBoulder/tiamat10-profile/compare/20240918...20240919
[20240918]: https://github.com/CuBoulder/tiamat10-profile/compare/20240911...20240918
[20240911]: https://github.com/CuBoulder/tiamat10-profile/compare/20240904...20240911
[20240904]: https://github.com/CuBoulder/tiamat10-profile/compare/20240821...20240904
[20240821]: https://github.com/CuBoulder/tiamat10-profile/compare/20240814...20240821
[20240814]: https://github.com/CuBoulder/tiamat10-profile/compare/20240805...20240814
[20240805]: https://github.com/CuBoulder/tiamat10-profile/compare/20240725...20240805
[20240725]: https://github.com/CuBoulder/tiamat10-profile/compare/20240719...20240725
[20240719]: https://github.com/CuBoulder/tiamat10-profile/compare/20240711...20240719
[20240711]: https://github.com/CuBoulder/tiamat10-profile/compare/20240612...20240711
[20240612]: https://github.com/CuBoulder/tiamat10-profile/compare/20240604...20240612
[20240604]: https://github.com/CuBoulder/tiamat10-profile/compare/20240513...20240604
[20240513]: https://github.com/CuBoulder/tiamat10-profile/compare/20240221...20240513
[20240221]: https://github.com/CuBoulder/tiamat10-profile/compare/20231212...20240221
[20231212]: https://github.com/CuBoulder/tiamat10-profile/compare/20230918...20231212
[20230918]: https://github.com/CuBoulder/tiamat10-profile/compare/b18a1906373a01be11ef84f9cb95d6b171aa9eab...20230918
