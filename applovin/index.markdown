# applovin.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__				[Library][api.type.Library]
> __Revision__			[REVISION_LABEL](REVISION_URL)
> __Keywords__			ads, advertising, AppLovin
> __Platforms__			Android, iOS
> __Sample__			[https://github.com/coronalabs/plugins-sample-applovin](https://github.com/coronalabs/plugins-sample-applovin)
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

* If you use the __AppLovin&nbsp;Free__ version and make changes to the ad settings in the [AppLovin developer portal](https://www.applovin.com/manage), you must also email [applovin-support@coronalabs.com](mailto:applovin-support@coronalabs.com) with a summary of your changes. This ensures that your ads and associated preferences will be delivered consistently.

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Check out new `setHasUserConsent` method to enable GDPR data collection restrictions.

</div>

## Versions

The AppLovin plugin is offered in two varieties, aimed to accommodate different Corona developers and business models:

<div class="docs-tip-outer" style="background-color: #ff7f4c;">
<div class="docs-tip-inner-left">
<div class="fa fa-user-circle-o" style="font-size: 28px; margin-top: 4px;"></div>
</div>
<div class="docs-tip-inner-right">

Monetization through the __AppLovin&nbsp;Free__ plugin entails a revenue share with Corona&nbsp;Labs in the form of a fixed 5% flat rate, but the ad revenue you see in your AppLovin dashboard is all yours.

</div>
</div>

<div class="docs-tip-outer docs-tip-color-alert">
<div class="docs-tip-inner-left">
<div class="fa fa-unlock-alt" style="font-size: 36px; margin-top: 2px; margin-left: 1px;"></div>
</div>
<div class="docs-tip-inner-right">

The __AppLovin&nbsp;Paid__ plugin lets you keep 100% of your ad revenue and allows you to manage your account/settings with AppLovin directly. It is only available to users who have purchased the [AppLovin Paid](https://marketplace.coronalabs.com/plugin/com.coronalabs/plugin.applovin.paid) plugin.

</div>
</div>


## Registration

To begin, please register with [AppLovin](https://www.applovin.com/signup). Once you have access to the [AppLovin developer portal](https://www.applovin.com/manage), you can view your apps, select ad preferences, and more.


## Syntax

<div id="example">

##### AppLovin Free

	local applovin = require( "plugin.applovin" )

##### AppLovin Paid

	local applovin = require( "plugin.applovin.paid" )

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

##### AppLovin Free

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

##### AppLovin Paid

``````{ brush="lua" gutter="false" first-line="1" highlight="[5,6,7,8]" }
settings =
{
	plugins =
	{
		["plugin.applovin.paid"] =
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
