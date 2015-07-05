# Layers Changelog

=======
## 1.2.1
### 03 July 2015

Hotfix for the new RTE feature

* **Fix** - The RTE now allows <script /> tags as not to affect
* **Fix** - Hiding of the text editor before initialization now uses a less specific class than .hide

=======
## 1.2.0
### 30 June 2015

Security updates, new RTE feature

* **Fix** - Tags in post meta all around the theme are now fixed
* **Feature** - Introducind the Rich Text Editor!
* **Security** - Added extra checks on the Theme Options partial loader logic
* **Security** - Decreased the usage of `extract` to avoid $GLOBAL[] overwrites in widget forms
* **Enhancement** - Changed concat method for echo functions in some files to enhance performance
* **Enhancement** - Up to 800% speed improvements on the initialization of the customizer

=======
## 1.1.5
### 05  June 2015

Hotfix

* **Fix** - Layers page imports are fixed for imports with a lot of JSON involved
* **Fix** - Post widget pagination now works when you're using the Post Widget in a non-front page page. Fixes #130
* **Fix** - Deleted `partials/portfolio-list.php`, it is unused
* **Fix** - Corrected the map pin when using Longitude and Latitude. Fixes #128
* **Fix** - When using just a link and link text in a content widget column, there is no need to enter in a blank excerpt to get the button to show
* **Fix** - Google Analytics in the Dashboard quick start now saves. Fixes #162
* **Fix** - Removed duplicate code for loading the the Widgets Initialization files.
* **Tweak** - Moved to MailChimp from Campaign Monitor for the newsletter signup form in the Layers Dash
* **Tweak** - DevKit and ColorKit mentions added to customizer
* **Enhancement** - Added bit.ly links to the dashboard marketplace buttons
* **Enhancement** - Each column in the content widget now gets a class which includes the columns $guid making for better CSS targeting
* **Enhancement** - Added `layers_before_blog_template` and `layers_after_blog_template` hooks to the `template-blog.php` page template
* **Enhancement** - Added `layers_after_single_title` hook and moved the `layers_before_single_title_meta` and `layers_after_single_title_meta` hooks inside the post meta if() conditional
* **Enhancement** - Added `layers_after_list_post_content` hook and moved the `layers_before_list_post_content` inside the content if() condition
* **Enhancement** - Added `layers_after_list_post_title` hook
* **Enhancement** - Added `layers_after_list_post_meta` hook
* **Enhancement** - Added `layers_before/after_site_description` hook
* **Enhancement** - Added `layers_after_comments` hook and moved comments hook into comments.php
* **Enhancement** - Moved `layers_before/after_title_heading` inside the `if()` condition which displays the title
* **Enhancement** - Added `layers_before/after_title_excerpt` in `/partials/header-page-title.php`
* **Enhancement** - Improved partial doc blocks and fixed up code formatting
* **Enhancement** - Removed errand ?> at the end of `get_footer();` in all archive and single files

=======
## 1.1.4
### 15  May 2015

Hotfix

* **Fix** - Leaving the `elements` argument for custom Design Bar items would throw an error, we've created a fallback for it
* **Fix** - Quotations in text fields are now properly escaped
* **Fix** - Fixed the post widget which was broken between 1.1.2 and 1.1.3
* **Fix** - Removed query strings from Layers custom font includes, this fixes the 404 issue some users experienced when loading the customizer
* **Fix** - WooCommerce column shortcodes no longer break
* **Enhancement** - Setting content widget to 12 columns no longer forces 745px max width on the excerpt container
* **Enhancement** - Added a filter to the `layers_inline_styles()` function, developers can now use the `layers_inline_' . $type . '_css` filter to add custom CSS  to the inline style generator
* **Enhancement** - Improved the instantiation of customizer defaults and color controls
* **Enhancement** - Added filter on the `layers_post_featured_media();` function to control the output of the HTML
* **Enhancement** - Better handling of animations in Safari

=======
## 1.1.3
### 01 May 2015

Post widget hotfix

* **Fix** - Post widget category selection is now fixed


=======
## 1.1.2
### 29 April 2015

New dashboard links, color helper file and form item support

* **Fix** - Added missing text domain to widget descriptions
* **Tweak** - Moved color helper functions into their own file, `/core/helpers/color.php`
* **Enhancement** - Added support for multi select boxes in `/core/helpers/form.php`, developers can use `multi-select` input type.

=======
## 1.1.1
### 23 April 2015

New color controls and much smarter handling of text colors, plus a brand new Layers Dashboard!

* **Tweak** - Dashboard edit
* **Fix** - Custom font variants now load correctly

=======
## 1.1.0
### 22 April 2015

New color controls and much smarter handling of text colors, plus a brand new Layers Dashboard!

* **Enhancement** - New Dashboard! The Layers Dashboard now has quick setup links, a live documentation search, plugin lists and a news feed
* **Enhancement** - Added column color support to the Post Widget
* **Enhancement** - All Widgets now get intelligent text coloring which responds to the light or darkness of your background colors
* **Enhancement** - Added button color selectors to the Post widget
* **Enhancement** - Added support for the 'target' attribute to the button form type
* **Enhancement** - Added .invert styling for headers
* **Enhancement** - Added 'border' option to the 'layers_inline_styles' function
* **Enhancement** - Added Site Accent color which affects all buttons and links
* **Enhancement** - Builder pages now obey password protection
* **Enhancement** - Slider now focusses on which ever slide you are busy editing
* **Enhancement** - If there is only a map widget on the page, it will sit flush with the header
* **Enhancement** - Improved support for WooCommerce price filter widget
* **Enhancement** - Improved default color settings for child themers
* **Enhancement** - Improved handling of 'layers_inline_styles()' which now uses 'func_num_args()'
* **Enhancement** - Added new Button controller to the design bar which affects button background colors along with 'layers_inline_button_styles()'
* **Enhancement** - Added more a dynamic class which handles the use of adding .invert to containers
* **Enhancement** - Added filters to the Layers sidebar classes
* **Enhancement** - Improved class handling in Layers widgets, each widget now has a much neater way of creating widget container classes
* **Fix** - Added better customizer default handling via the 'layers_customizer_control_defaults' hook
* **Fix** - Logo Center with no menu no longer breaks
* **Fix** - Payment method block alignment no longer has a margin on the left
* **Fix** - Pagination location on the post widget
* **Fix** - Clicking the canvas in the customizer now closes widgets using the customizer API
* **Fix** - Gutter option on all widgets with masonry active now works
* **Fix** - .pull-right problem where adding it to a .column was not forcing float: right;
* **Fix** - .upsells now align properly on desktop and mobile
* **Fix** - Tag archive pages
* **Fix** - Layers pages set to password protected now require a password to view
* **Fix** - Slider image-center + text right will now align all text correctly
* **Fix** - Removing your logo no longer leaves a broken image
* **Fix** - WooCommerce product tag archives now have the correct styling
* **Fix** - Slider 'layout-full-screen' not working - if auto height is not checked then slider hard sets height which stops full-screen working
* **Tweak** - Header cart background color has changed for a hash value to a transparent rgba background color for better handling of different header colors
* **Tweak** - Improved spacing of the comment form block as well as a font-size decrease for "Leave a Reply"
* **Tweak** - Gave copyright border-color rgba (same reason as header cart)
* **Tweak** - Better .button styling in .story
* **Tweak** - Increased the width of sub menus
* **Tweak** - Nested comments now clear the .copy div in the parent comment
* **Tweak** - The 'search' button in the Search Widget is now inline with the input field on screens larger than tablets
* **Tweak** - Bread crumbs css is now based on RGBA for better handling of container background colors
* **Tweak** - Bread crumbs css now included in .invert class
* **Tweak** - Removed color from headings in .story and .copy as they are already declared as defaults at the top of the CSS
* **Tweak** - All color settings (Header and Footer included) are now find under Site Settings > Colors
* **Tweak** - Escaped 'add_query_arg()' as possible security flaw was recently identified
* **Notice** - Layers 1.0.9 has full WordPress 4.2 compatability


## 1.0.8
### 02 April 2015

Hotfix for the Slider responsive CSS

* **Fix** - Update 1.0.7 broke sliders in phone view, this fixes that, slides now behave as in 1.0.6

## 1.0.7
### 02 April 2015

Layers page Import / Export fix

* **Tweak** - Changed the way the Layers customizer menu is constructed in render_customizer_menu() to make it more extendible
* **Tweak** - WooCommerce CSS tweaks on product-single
* **Tweak** - Slider CSS tweaks
* **Fix** - When adding a new standard page and selecting the Layers Template without clicking save the customizer would throw a 404, now we force users to click save first
* **Fix** - Page exports would occasionally cause users to reach a 'Warning: headers already sent by' error, we've fixed this error by moving the export trigger
* **Fix** - The page import button would fail with a JSON not allowed error, we have added json and JSON to allowed file types to counteract this problem
* **Fix** - When switching to a Layers child theme, customizer settings are now kept alive and transferred to your child theme
* **Enhancement** - Widget placeholder text is now translatable
* **Enhancement** - Added hooks to title container, posts and pages


## 1.0.6
### 20 March 2015

Patch fix which fixes the order of the custom CSS implementation

* **Fix** - Star ratings no longer bump to the top right of the page on WooCommerce product single pages
* **Enhancement** - Added four new icons to admin font - desktop, tablet, iphone and tick
* **Tweak** - Moved 'layers-custom-styles' enqueue to it's own action in the footer to make sure it loads last
* **Tweak** - Bail if no css is generated by layers_inline_styles()
* **Tweak** - Moved 'layers_inline_css' filter to layers_apply_inline_styles()

## 1.0.5
### 19 March 2015

Bug fixes and language additions

* **Tweak** - Changed the "Page Builder" page template to "Layers Template"
* **Enhancement** - Added the ability to bypass the built-in Customizer sanitization
* **Fix** - Unchecking all post meta display not longer causes all of the options to actually display
* **Enhancement** - Added new dropdown to customizer so that users can easily navigate back to dashboard, create new page and preview page
* **Enhancement** - Added the "range" option to the Form->input() function
* **Enhancement** - Added Chinese translation files
* **Enhancement** - Added Turkish translation files
* **Enhancement** - Added German translation files
* **Enhancement** - Added Spanish translation files
* **Fix** - When adding a single top menu, the opposite menu no long defaults to show pages
* **Fix** - Added license information to swiper.js
* **Fix** - WooCommerce pages no longer have a spacing issue when right sidebar is turned on
* **Fix** - .sub-menu width in off-canvas menu has been fixed to avoid text-wrapping
* **Fix** - Dots from payment methods in Woo checkout page have been removed
* **Fix** - Grouped product styling in WooCommerce has been fixed
* **Fix** - The large gap appearing above a sticky header when you're logged in on a mobile phone no longer appears
* **Fix** - Fixed when clicking any widget design bar sub menu would erroneously deselect active states of all the controls visual selectors
* **Tweak** - Text change 'Editing widget content' slide
* **Tweak** - Removed unused WooCommerce CSS and placed them in new pro woo extension
* **Tweak** - get_theme_mod( 'custom-css' ); no longer uses layers_inline_style, this is in preparation of PostMessage support
* **Tweak** - Clicking anywhere on the page will close any open design bar sub menus
* **Tweak** - Stop persistent Layers page filtering in page list, choosing all would confusingly show only Layers pages

## 1.0.4
### 02 March 2015

Security and code quality updates

* **Enhancement** - Added 'range' type to the form options
* **Enhancement** - Added filtering to the design bar setup per widget (thanks @kevinlangleyjr)
* **Enhancement** - Improved class initiators (thanks @prettyboymp)
* **Enhancement** - Added filters to design bar components (thanks @prettyboymp)
* **Enhancement** - Clicking out of the design bar closes a control (thanks @prettyboymp @jeffstieler)
* **Enhancement** - Added customizer-preview.js for scripts executed in the customizer preview iframe only
* **Fix** - Deleting all slides then adding your first slide again threw an error (thanks @prettyboymp)
* **Fix** - Fix references from i8n to i18n
* **Fix** - Added check_ajax_referer() for Ajax nonceing
* **Fix** - Removed double <title /> tag
* **Fix** - Improved nonce handling and removed any reference to $_REQUEST[] in the code
* **Fix** - Updated Google maps API link for SSL compatability (thanks @oskapt)
* **Fix** - Improved localization (thanks @tmconnect)
* **Fix** - Added sanitization helpers which we hook into the customizer to clean up the Customizer data
* **Tweak** - Added Typekit ID field to the Site Settings, this means that getting Typekit into Layers is now even easier and safer
* **Tweak** - Move hooks and filters outside of their related function_exists closures
* **Tweak** - Replaced deprecated get_page() with get_post()
* **Tweak** - Added version number to all css and js assets being enqueued
* **Tweak** - Added nonce check and remove unnecessary conditional from to update_page_builder_meta()
* **Tweak** - .media block (used extensively in the content widget html) has been tweaked to behave better on different screensizes and with different column widths
* **Tweak** - Changed jquery-masonry to masonry v3 not dependent on jquery
* **Tweak** - Updated hook used for meta box registration
* **Tweak** - Changed in-line styles and scripts to always use admin_print_styles and admin_print_scripts hooks
* **Tweak** - Moved fouc rendering issue fix from in-line to the customizer-preview.js
* **Tweak** - Slider behaves better in responsive mode - no longer image/copy overlap
* **Tweak** - Apply class to Slider for layout eg slider-layout-full-screen and a unique not-full-screen
* **Tweak** - Merged color.css typography.css and framework.css so that fewer style sheets are loaded, therefore improved load times

## 1.0.3
### 23 February 2015

Post-launch bug fixes before settling into a release schedule

* **Fix** - Portfolio preset template now works correctly (thanks @nitinthewiz)
* **Tweak** - Removed layers_site_title(); function in favor of WordPress built in site title function
* **Tweak** - Added <?php get_search_form(); ?> to the 404 page
* **Fix** - Product page styling with sidebars is now correct (thanks @luizbills)
* **Tweak** - Added target=_blank on the Built With Layers badge
* **Fix** - Fixed the Layers dashboard header


## 1.0.2
### 20 February 2015

Theme Check requirements and url updates

* **Fix** - Added sprintf() to any hard coded urls
* **Fix** - Corrected all Layers Dashboard urls
* **Fix** - Removed unuses scripts from /assets/js/
* **Fix** - Fixed 404 page styling

## 1.0.1
### 19 February 2015

Some quick fixes that help improve the overall experience

* **Tweak** - Removed un-needed scripts from loading on the front-end
* **Fix** - Removed un-used images from the /assets/css/images folder
* **Tweak** - Added a notice to download the Layers Updater to the Layers Dashboard
* **Tweak** - Cleaned up third party JS scripts
* **Fix** - Removed unused WooCommerce Sidebars
