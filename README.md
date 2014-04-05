Google Tag Manager Import Export Greasemonkey script
=================

The script will allow you to export and import tags, rules and macros between
different GTM accounts and containers.


## Installation


This script is only supported in Firefox and Greasemonkey. 

 1. Install [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/)
 2. Go to https://github.com/maschek/gtm_import_export/raw/master/Google_Tag_Manager_Import_Export.user.js and install the script into Greasemonkey.

## Usage

Once installed, go to your GTM account and observe the new interface elements:

![](https://github.com/maschek/gtm_import_export/raw/master/images/overview.png)

### Exporting and importing

1. Choose the tab you want to export (tags, rules or macros)
2. Check the checkboxes of the elements you want to export, or use [Select/deselect all] button
3. Click on [Export selected]
4. The result of the export will appear in the top right textarea. Copy the content of this into your clipboard.
5. Navigate to the account or container you want to import into
6. Navigate to the tab what you want to import (Tag, Rule or Macro)
7. Paste your clipboard content into the top right textarea
8. Hit import button
9. Notice the messages in the top left textarea. If something went wrong, you will see here.

Note: Only visible elements will be exported. To export all pages, you have to manually switch pages and export again.

Supported tags:
* Custom HTML Tag
* Custom Image Tag
* AdWords Conversion Tracking


Supported rules:
* ALL

Supported macros:
* CUSTOM_VAR
* COOKIE
* AUTO_EVENT_VAR
* CONSTANT
* EVENT
* ARBITRARY_JAVASCRIPT
* DOM_ELEMENT
* REFERRER
* URL

Unsupported elements will simply be skipped during export.

### Exporting a whole container

To export a whole container into another one, you have to export/import the elements in the following order:
1. Export/import all Macros
2. Export/import all Rules
3. Export/import all Tags

## Issues

Open your issues here:
https://github.com/maschek/gtm_import_export/issues

