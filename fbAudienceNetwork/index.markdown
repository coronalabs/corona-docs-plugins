# fbAudienceNetwork.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, Facebook Audience Network, fbAudienceNetwork
> __Platforms__			Android, iOS
> __Sample__			[https://github.com/coronalabs/plugins-sample-fbAudienceNetwork](https://github.com/coronalabs/plugins-sample-fbAudienceNetwork)
> --------------------- ------------------------------------------------------------------------------------------


## Overview

The Facebook Audience Network plugin allows developers to monetize their mobile app with Facebook banner, rewarded and static interstitial ads.

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Facebook has a method for calling test ads which is different from other Corona ad providers. To test ads during implementation of this plugin, you must follow their requirements. Please read the notes in the [fbAudienceNetwork.init()][plugin.fbAudienceNetwork.init] documentation and follow the steps to enable test ads.

</div>


## Versions

The Facebook Audience Network plugin is offered in two varieties, aimed to accommodate different Corona developers and business models:

<div class="docs-tip-outer" style="background-color: #ff7f4c;">
<div class="docs-tip-inner-left">
<div class="fa fa-user-circle-o" style="font-size: 28px; margin-top: 4px;"></div>
</div>
<div class="docs-tip-inner-right">

Monetization through the __Facebook Audience Network&nbsp;Free__ plugin entails a revenue share with Corona&nbsp;Labs in the form of a fixed 5% flat rate, but the ad revenue you see in your [Facebook Developer Portal](https://developers.facebook.com/apps/) is all yours.

</div>
</div>

<div class="docs-tip-outer docs-tip-color-alert">
<div class="docs-tip-inner-left">
<div class="fa fa-unlock-alt" style="font-size: 36px; margin-top: 2px; margin-left: 1px;"></div>
</div>
<div class="docs-tip-inner-right">

The __Facebook Audience Network&nbsp;Paid__ plugin lets you keep 100% of your ad revenue. It is only available to users who have purchased the [Facebook Audience Network Paid](https://marketplace.coronalabs.com/plugin/facebook-audience-network-paid) plugin.

</div>
</div>


## Registration

Before you can use the Facebook Audience Network, you must set up [Audience Network](https://developers.facebook.com/docs/audience-network/getting-started) in your app.


## Syntax

<div id="example">

##### Facebook Audience Network Free

	local fbAudienceNetwork = require( "plugin.fbAudienceNetwork" )

##### Facebook Audience Network Paid

	local fbAudienceNetwork = require( "plugin.fbAudienceNetwork.paid" )

</div>


## Functions

#### [fbAudienceNetwork.init()][plugin.fbAudienceNetwork.init]

#### [fbAudienceNetwork.show()][plugin.fbAudienceNetwork.show]

#### [fbAudienceNetwork.hide()][plugin.fbAudienceNetwork.hide]

#### [fbAudienceNetwork.getSize()][plugin.fbAudienceNetwork.getSize]

#### [fbAudienceNetwork.isLoaded()][plugin.fbAudienceNetwork.isLoaded]

#### [fbAudienceNetwork.load()][plugin.fbAudienceNetwork.load]


## Events

#### [adsRequest][plugin.fbAudienceNetwork.event.adsRequest]


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

<div id="example">

##### Facebook Audience Network Free

``````{ brush="lua" gutter="false" first-line="1" highlight="[5,6,7,8]" }
settings =
{
	plugins =
	{
		["plugin.fbAudienceNetwork"] =
		{
			publisherId = "com.coronalabs"
		},
	},
}
``````

##### Facebook Audience Network Paid

``````{ brush="lua" gutter="false" first-line="1" highlight="[5,6,7,8]" }
settings =
{
	plugins =
	{
		["plugin.fbAudienceNetwork.paid"] =
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
* `"android.permission.ACCESS_WIFI_STATE"`

</div>
