# chartboost.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, Chartboost
> __Platforms__			Android, iOS
> --------------------- ------------------------------------------------------------------------------------------

## Overview

The Chartboost plugin allows developers to monetize users through [Chartboost](https://www.chartboost.com) static interstitial, video interstitial, rewarded video ads, and more.

<div class="docs-tip-outer docs-tip-color-alert">
<div class="docs-tip-inner-left">
<div class="fa fa-unlock-alt" style="font-size: 36px; margin-top: 2px; margin-left: 1px;"></div>
</div>
<div class="docs-tip-inner-right">

The Chartboost plugin is only available to users who have purchased the [Corona Professional Bundle](https://marketplace.coronalabs.com/products/corona-pro) or the [Chartboost](https://marketplace.coronalabs.com/plugin/chartboost) plugin. This plugin lets you keep 100% of your ad revenue and allows you to manage your account/settings with Chartboost directly.

</div>
</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Check out new `hasUserConsent` init parameter to enable GDPR data collection restrictions.

</div>

## Registration

Before you can use this plugin, you must [register](https://www.chartboost.com ) with Chartboost.


## Syntax

	local chartboost = require( "plugin.chartboost" )


## Functions

#### [chartboost.init()][plugin.chartboost.init]

#### [chartboost.load()][plugin.chartboost.load]

#### [chartboost.isLoaded()][plugin.chartboost.isLoaded]

#### [chartboost.show()][plugin.chartboost.show]

#### [chartboost.onBackPressed()][plugin.chartboost.onBackPressed]


## Events

#### [adsRequest][plugin.chartboost.event.adsRequest]


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````lua
settings =
{
	plugins =
	{
		["plugin.chartboost"] =
		{
			publisherId = "com.coronalabs"
		},
	},
}
``````

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

If you are building for Android, you should __remove__ any legacy inclusion of the `["plugin.google.play.services"]` plugin from your `build.settings`.

</div>

<div class="guide-notebox">
<div class="notebox-title">Note</div>

For Android, the following permissions/features are automatically added when using this plugin:

* `"android.permission.INTERNET"`
* `"android.permission.ACCESS_NETWORK_STATE"`
* `"android.permission.WRITE_EXTERNAL_STORAGE"`

In addition, you can add the following optional (but&nbsp;recommended) permissions:

* `"android.permission.ACCESS_WIFI_STATE"` &mdash; Allows the Chartboost SDK to check WiFi details and send the MAC address in the HTTP request. This will be used alongside the Android ID and/or GAID (where&nbsp;applicable) as the identifier for the user.

* `"android.permission.READ_PHONE_STATE"` &mdash; Allows the Chartboost SDK to handle calls interrupting video playback during videos.

</div>


## Support

* [https://answers.chartboost.com/](https://answers.chartboost.com/)
* [Corona Forums](http://forums.coronalabs.com/forum/545-monetization-in-app-purchases-ads-etc/)
