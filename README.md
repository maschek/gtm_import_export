# Archiving this repo as GTM updated their UI many years ago and AFAIK they also solved the export/import problem.


Google Tag Manager Import Export Greasemonkey script
=================

The script will allow you to export and import tags, rules and macros between
different GTM accounts and containers.


## Installation


This script is supported in Firefox and Greasemonkey or Chrome and Tampermonkey. 

 1. Install [Greasemonkey for Firefox](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/) or [Tampermonkey for Chrome](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en)
 2. Go to https://github.com/maschek/gtm_import_export/raw/master/Google_Tag_Manager_Import_Export.user.js and install the script into Greasemonkey/Tampermonkey.

## Usage

Once installed, go to your GTM account and observe the new interface elements:

![](https://github.com/maschek/gtm_import_export/raw/master/images/overview.png)

### Exporting and importing

1. Choose the tab you want to export (tags, rules or macros)
2. Check the checkboxes of the elements you want to export, or use [Select/deselect all] button
3. Click on [Export selected]
4. The result of the export will appear in the top right textarea. Copy the content of this into your clipboard.
5. Navigate to the target account or container you want to import into
6. Navigate to the tab what you want to import (Tag, Rule or Macro)
7. Paste your clipboard content into the top right textarea
8. Hit import button
9. Notice the messages in the top left textarea. If something went wrong, you will see here.

Notes:
* Only visible elements will be exported. To export all pages, you have to manually switch pages and export again.
* If a tag has a rule that is not present in the target container, the tag will be imported without the rule. You must first  import the required rules to avoid this.
* Similarly, if a rule depends on a macro that is not present in the target container, you will have to import the macro first.

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

Update:
Google has developed a full container import/export functionality. You can read how it works here:
https://support.google.com/tagmanager/answer/4540826?hl=en

## Issues

Open your issues here:
https://github.com/maschek/gtm_import_export/issues

## Donate

If you found the script useful, why not consider a paypal donation?
[Go to PayPal] (https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=adam%2emaschek%40gmail%2ecom&lc=US&item_name=Google%20Tag%20Manager%20script&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donate_LG%2egif%3aNonHosted)
