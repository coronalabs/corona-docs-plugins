# applovin.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__				[Library][api.type.Library]
> __Revision__			[REVISION_LABEL](REVISION_URL)
> __Keywords__			ads, advertising, AppLovin
> __Platforms__			Android, iOS
> --------------------- ------------------------------------------------------------------------------------------


## Overview

<!---

<div class="float-right" style="max-width: 240px; clear: both;">

![][images.docs.plugin-screenshot-applovin]

</div>

-->

The AppLovin plugin allows developers to monetize users through [AppLovin](https://www.applovin.com/) static interstitial, video interstitial, and rewarded video ads.

<div class="guide-notebox">
<div class="notebox-title">Notes</div>

* Once you are [registered](https://www.applovin.com/signup), obtain your __SDK&nbsp;key__ from the [AppLovin developer portal](https://www.applovin.com/manage). From the __Account__ section, expand the __Account__ menu on the left side, select __Keys__, and your SDK key should be revealed.

* Native ads are not supported at this time.

* Apps are automatically added to the [AppLovin developer portal](https://www.applovin.com/manage) when you [include](#settings) this plugin within your project, `require()`&nbsp;it, and call [applovin.init()][plugin.applovin.init].

* If you use the plugin and make changes to the ad settings in the [AppLovin developer portal](https://www.applovin.com/manage), you must also email [support@solar2d.com](mailto:support@solar2d.com) with a summary of your changes. This ensures that your ads and associated preferences will be delivered consistently.

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Check out new `setHasUserConsent` method to enable GDPR data collection restrictions.

</div>

## Registration

To begin, please register with [AppLovin](https://www.applovin.com/signup). Once you have access to the [AppLovin developer portal](https://www.applovin.com/manage), you can view your apps, select ad preferences, and more.


## Syntax

<div id="example">

##### AppLovin

	local applovin = require( "plugin.applovin" )

</div>


## Functions

#### [applovin.init()][plugin.applovin.init]

#### [applovin.load()][plugin.applovin.load]

#### [applovin.isLoaded()][plugin.applovin.isLoaded]

#### [applovin.show()][plugin.applovin.show]

#### [applovin.setUserDetails()][plugin.applovin.setUserDetails]

#### [applovin.hide()][plugin.applovin.hide]

#### [applovin.setHasUserConsent()][plugin.applovin.setHasUserConsent]


## Events

#### [adsRequest][plugin.applovin.event.adsRequest]


<a id="settings"></a>

## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

<div id="example">

##### AppLovin

``````{ brush="lua" gutter="false" first-line="1" highlight="[5,6,7,8]" }
settings =
{
	plugins =
	{
		["plugin.applovin"] =
		{
			publisherId = "com.coronalabs"
		},
	},
}
``````

</div>

<div class="guide-notebox">
<div class="notebox-title">Note</div>

For Android, the following permissions/features are automatically added when using this plugin:

* `"android.permission.INTERNET"`
* `"android.permission.ACCESS_NETWORK_STATE"`
* `"android.permission.WRITE_EXTERNAL_STORAGE"`

</div>

## Sample project

* [View on GitHub](https://github.com/coronalabs/plugins-sample-applovin)
