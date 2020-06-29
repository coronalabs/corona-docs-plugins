# appodeal.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, Appodeal
> __Platforms__			Android, iOS
> __Sample__			[https://github.com/coronalabs/plugins-sample-appodeal](https://github.com/coronalabs/plugins-sample-appodeal)
> --------------------- ------------------------------------------------------------------------------------------


## Overview

The Appodeal plugin allows developers to monetize their mobile app with Appodeal banner, static interstitial, video interstitial, and rewarded video ads.

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Be warned that plugin builds for Amazon store are restricted at the moment. We are working on the appropriate SDK/plugin update and the ability to publish your apps, which includes Corona Appodeal modular plugin, to Amazon store should become available as soon as possible.

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Appodeal contains various SDKs for the ad providers it mediates. This means that you can __not__ use Appodeal in conjunction with [AdColony][plugin.adcolony], [AppLovin][plugin.applovin], [AdMob][plugin.admob], [Chartboost][plugin.chartboost], [Facebook Audience Network][plugin.fbAudienceNetwork], [Flurry Analytics][plugin.flurry-analytics], [InMobi][plugin.inmobi], [Unity Ads][plugin.unityads], or [Vungle][plugin.vungle].

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Beta version of Corona Appodeal plugin is now available! Check latest note in Project Settings section to learn more.

#### Version info
Current plugin versions are:

* Both stable and beta plugins are `2.6.4` for both Android and iOS (if using daily build `2020.3569` or later).

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Check out new `hasUserConsent` init parameter to enable GDPR data collection restrictions.

</div>


## Registration

Before you can use this plugin, you must [register](https://www.appodeal.com/signup) with Appodeal.


## Syntax

	local appodeal = require( "plugin.appodeal" )


## Functions

#### [appodeal.init()][plugin.appodeal.init]

#### [appodeal.show()][plugin.appodeal.show]

#### [appodeal.hide()][plugin.appodeal.hide]

#### [appodeal.load()][plugin.appodeal.load]

#### [appodeal.isLoaded()][plugin.appodeal.isLoaded]

#### [appodeal.setUserDetails()][plugin.appodeal.setUserDetails]

#### [appodeal.getRewardParameters()][plugin.appodeal.getRewardParameters]

#### [appodeal.getVersion()][plugin.appodeal.getVersion]

#### [appodeal.setSegmentFilter()][plugin.appodeal.setSegmentFilter]

#### [appodeal.canShow()][plugin.appodeal.canShow]

#### [appodeal.trackInAppPurchase()][plugin.appodeal.trackInAppPurchase]

#### [appodeal.set728x90Banners()][plugin.appodeal.set728x90Banners]


## Events

#### [adsRequest][plugin.appodeal.event.adsRequest]


## Project Settings

To use this plugin in modular mode, your `plugins` table of `build.settings` should look like this:

``````lua
settings =
{
	iphone =
	{
		plist =
		{
			GADApplicationIdentifier = "ca-app-pub-3940256099942544~1458002511", -- replace with your app id. See: https://googlemobileadssdk.page.link/admob-ios-update-plist
		},
	},
	android =
	{
		applicationChildElements =
		{
			[[
				<meta-data android:name="com.google.android.gms.ads.APPLICATION_ID"
					android:value="[YOUR_ADMOB_APP_ID]"/>  -- replace with your app id. See: https://goo.gl/fQ2neu
			]],
		},
	},
	plugins =
	{
		-- Base
		['plugin.appodeal.base'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.GoogleAdMob'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },

		-- Banner
		['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Yandex'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.AmazonAds'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.TwitterMoPub'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Smaato'] = { publisherId = 'com.coronalabs' },

		-- Interstitial
		['plugin.appodeal.AdColony'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Chartboost'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.IronSource'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Mobvista'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Ogury'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.AmazonAds'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.TwitterMoPub'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Smaato'] = { publisherId = 'com.coronalabs' },

		-- Rewarded Video
		['plugin.appodeal.AdColony'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Chartboost'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.IronSource'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Mobvista'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Unity'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Vungle'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Tapjoy'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.TwitterMoPub'] = { publisherId = 'com.coronalabs' },
	},
}
``````

Make sure to include `Base` block for a plugin to work correctly. Then you can just comment out unnecessary ad types blocks, so that unneded adapters are not downloaded and linked to your project.

<div class="guide-notebox">
<div class="notebox-title">Note</div>

Disabling specific ad types and ad providers at this level with the help of new modular structure can greatly reduce the final build size.

</div>

For example, if you don't use Interstitials or Rewarded Video ad types in your app, you can comment blocks:

``````lua
-- Interstitial
--['plugin.appodeal.AdColony'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Chartboost'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.IronSource'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Mobvista'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Ogury'] = { publisherId = 'com.coronalabs' },

-- Rewarded Video
--['plugin.appodeal.AdColony'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Chartboost'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.IronSource'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Mobvista'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Unity'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Vungle'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Tapjoy'] = { publisherId = 'com.coronalabs' },
``````

If for some reason you don't want to show ads from specific ad provider (for the sake of example, let it be `Flurry`), you can comment out it too, like this:

``````lua
-- Banner
['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
--['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.Yandex'] = { publisherId = 'com.coronalabs' },
``````

If you are sure of your choice and want to keep your build settings nice and clean, you can remove commented ad types or/and adapters. Then for this particular example your build.settings file should look like this:

``````lua
-- Base
['plugin.appodeal.base'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.GoogleAdMob'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },

-- Banner
['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.Yandex'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.AmazonAds'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.TwitterMoPub'] = { publisherId = 'com.coronalabs' },
``````
<div class="guide-notebox">
<div class="notebox-title">Note</div>

From now on, you can use a beta version of modular plugin system. It includes the latest Appodeal SDK Beta, some new features and improvements. To use it, you should add a `beta` tag to module declaration like this, for example:

``````lua
settings =
{
	android =
	{
		applicationChildElements =
		{
			[[
				<meta-data android:name="com.google.android.gms.ads.APPLICATION_ID"
					android:value="[YOUR_ADMOB_APP_ID]"/>  -- replace with your app id. See: https://goo.gl/fQ2neu
			]],
		},
	},
	plugins =
	{
		['plugin.appodeal.beta.base'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.AdColony'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.AmazonAds'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.AppLovin'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Appnext'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Chartboost'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.FacebookAudience'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Flurry'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.GoogleAdMob'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.InMobi'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.IronSource'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Mobvista'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.MyTarget'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Ogury'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.StartApp'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Tapjoy'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.TwitterMoPub'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Unity'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Vungle'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.beta.Yandex'] = { publisherId = 'com.coronalabs' },
	},
}
``````

Please keep in mind, that using beta versions of both Appodeal SDK and Corona Appodeal plugin may cause unexpected issues. We've made a profound tests of a new system, but you should use it at your own risk.

</div>

<!--- Include ATS "override" template block --->
TEMPLATE_ATS
<!--- --->

<div class="guide-notebox">
<div class="notebox-title">Note</div>

For Android, the following permissions/features are automatically added when using this plugin:

* `"android.permission.INTERNET"`
* `"android.permission.ACCESS_NETWORK_STATE"`
* `"android.permission.WRITE_EXTERNAL_STORAGE"`

In addition, if you wish to receive targeted ads in your app and increase your chances for higher revenue, you can include any or all of the following permissions:

* `"android.permission.GET_ACCOUNTS"`
* `"android.permission.ACCESS_COARSE_LOCATION"`
* `"android.permission.ACCESS_FINE_LOCATION"`

</div>
