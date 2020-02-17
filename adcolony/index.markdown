# adcolony.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, AdColony
> __Platforms__			Android, iOS
> --------------------- ------------------------------------------------------------------------------------------

## Overview

The AdColony plugin allows developers to monetize users through [AdColony](http://www.adcolony.com) video interstitial and rewarded video ads.

<div class="docs-tip-outer docs-tip-color-alert">
<div class="docs-tip-inner-left">
<div class="fa fa-unlock-alt" style="font-size: 36px; margin-top: 2px; margin-left: 1px;"></div>
</div>
<div class="docs-tip-inner-right">

The AdColony plugin is only available to users who have purchased the [Corona Professional Bundle](https://marketplace.coronalabs.com/products/corona-pro) or the [AdColony](https://marketplace.coronalabs.com/plugin/adcolony) plugin. This plugin lets you keep 100% of your ad revenue and allows you to manage your account/settings with AdColony directly.

</div>
</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Check out new `hasUserConsent`  init parameter to enable GDPR data collection restrictions.

</div>


## Registration

Before you can use this plugin, you must [register](https://www.adcolony.com ) with AdColony.


## Syntax

	local adcolony = require( "plugin.adcolony" )


## Functions

#### [adcolony.init()][plugin.adcolony.init]

#### [adcolony.load()][plugin.adcolony.load]

#### [adcolony.isLoaded()][plugin.adcolony.isLoaded]

#### [adcolony.show()][plugin.adcolony.show]

#### [adcolony.getInfoForZone()][plugin.adcolony.getInfoForZone]


## Events

#### [adsRequest][plugin.adcolony.event.adsRequest]


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````lua
settings =
{
	plugins =
	{
		["plugin.adcolony"] =
		{
			publisherId = "com.coronalabs"
		},
	},
}
``````

### iOS

If your app is for iOS, you must also include the following code in `build.settings` to ensure that AdColony functions as intended:

``````lua
settings = {
 
	iphone =
	{
		plist =
		{
			LSApplicationQueriesSchemes =
			{
				"fb",
				"instagram",
				"tumblr",
				"twitter"
			},
			NSCalendarsUsageDescription = "This app would like to add events to the calendar.",
			NSPhotoLibraryUsageDescription = "This app would like to access the photo library.",
			NSCameraUsageDescription = "This app would like to access the camera.",
			NSMotionUsageDescription = "This app would like to use interactive ad controls."
		}
	}
}
``````

<!--- Include ATS "override" template block --->
TEMPLATE_ATS
<!--- --->

### Android

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

For Android, you should __remove__ any legacy inclusion of the `["plugin.google.play.services"]` plugin from your `build.settings`.

</div>

<div class="guide-notebox">
<div class="notebox-title">Note</div>

For Android, the following permissions/features are automatically added when using this plugin:

* `"android.permission.INTERNET"`
* `"android.permission.ACCESS_NETWORK_STATE"`
* `"android.permission.WRITE_EXTERNAL_STORAGE"`

In addition, you can add the following optional permissions:

* `"android.permission.VIBRATE"`

</div>


## Support

* [http://support.adcolony.com/](http://support.adcolony.com/)
* [Corona Forums](http://forums.coronalabs.com/forum/545-monetization-in-app-purchases-ads-etc/)
