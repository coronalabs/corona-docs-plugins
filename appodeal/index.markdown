# appodeal.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, Appodeal
> __Platforms__			Android, iOS
> --------------------- ------------------------------------------------------------------------------------------


## Overview

The Appodeal plugin allows developers to monetize their mobile app with Appodeal banner, static interstitial, video interstitial, and rewarded video ads.

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Be warned that plugin builds for Amazon store are restricted at the moment. We are working on the appropriate SDK/plugin update and the ability to publish your apps, which includes Appodeal modular plugin, to Amazon store should become available as soon as possible.

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Appodeal contains various SDKs for the ad providers it mediates. This means that you can __not__ use Appodeal in conjunction with [AdColony][plugin.adcolony], [AppLovin][plugin.applovin], [AdMob][plugin.admob], [Chartboost][plugin.chartboost], [Facebook Audience Network][plugin.fbAudienceNetwork], [Flurry Analytics][plugin.flurry-analytics], [InMobi][plugin.inmobi], [Unity Ads][plugin.unityads], or [Vungle][plugin.vungle].

</div>

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Beta version of Appodeal plugin is now available! Check latest note in Project Settings section to learn more.

#### Version info
Current plugin versions are:

* Stable plugins is `2.8.1` for both Android and iOS (if using daily build `2020.3569` or later). Beta plugin is not recommended to use and contains legacy version

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
			GADApplicationIdentifier = "[YOUR_ADMOB_APP_ID]", -- replace with your app id. See: https://googlemobileadssdk.page.link/admob-ios-update-plist
			NSAppTransportSecurity = { NSAllowsArbitraryLoads=true },
			NSLocationWhenInUseUsageDescription = "The app needs your location for analytics and advertising purposes",
			NSCalendarsUsageDescription = "The app needs your calendar to provide personalised advertising experience tailored to you",
			NSUserTrackingUsageDescription = "This identifier will be used to deliver personalized ads to you.",
			SKAdNetworkItems = {
				{ SKAdNetworkIdentifier = "4pfyvq9l8r.skadnetwork" },
				{ SKAdNetworkIdentifier = "yclnxrl5pm.skadnetwork" },
				{ SKAdNetworkIdentifier = "v72qych5uu.skadnetwork" },
				{ SKAdNetworkIdentifier = "tl55sbb4fm.skadnetwork" },
				{ SKAdNetworkIdentifier = "t38b2kh725.skadnetwork" },
				{ SKAdNetworkIdentifier = "prcb7njmu6.skadnetwork" },
				{ SKAdNetworkIdentifier = "ppxm28t8ap.skadnetwork" },
				{ SKAdNetworkIdentifier = "mlmmfzh3r3.skadnetwork" },
				{ SKAdNetworkIdentifier = "klf5c3l5u5.skadnetwork" },
				{ SKAdNetworkIdentifier = "hs6bdukanm.skadnetwork" },
				{ SKAdNetworkIdentifier = "c6k4g5qg8m.skadnetwork" },
				{ SKAdNetworkIdentifier = "9t245vhmpl.skadnetwork" },
				{ SKAdNetworkIdentifier = "9rd848q2bz.skadnetwork" },
				{ SKAdNetworkIdentifier = "8s468mfl3y.skadnetwork" },
				{ SKAdNetworkIdentifier = "7ug5zh24hu.skadnetwork" },
				{ SKAdNetworkIdentifier = "4fzdc2evr5.skadnetwork" },
				{ SKAdNetworkIdentifier = "4468km3ulz.skadnetwork" },
				{ SKAdNetworkIdentifier = "3rd42ekr43.skadnetwork" },
				{ SKAdNetworkIdentifier = "2u9pt9hc89.skadnetwork" },
				{ SKAdNetworkIdentifier = "m8dbw4sv7c.skadnetwork" },
				{ SKAdNetworkIdentifier = "7rz58n8ntl.skadnetwork" },
				{ SKAdNetworkIdentifier = "ejvt5qm6ak.skadnetwork" },
				{ SKAdNetworkIdentifier = "5lm9lj6jb7.skadnetwork" },
				{ SKAdNetworkIdentifier = "44jx6755aq.skadnetwork" },
				{ SKAdNetworkIdentifier = "mtkv5xtk9e.skadnetwork" },
				{ SKAdNetworkIdentifier = "ludvb6z3bs.skadnetwork" },
				{ SKAdNetworkIdentifier = "wg4vff78zm.skadnetwork" },
				{ SKAdNetworkIdentifier = "737z793b9f.skadnetwork" },
				{ SKAdNetworkIdentifier = "ydx93a7ass.skadnetwork" },
				{ SKAdNetworkIdentifier = "w9q455wk68.skadnetwork" },
				{ SKAdNetworkIdentifier = "glqzh8vgby.skadnetwork" },
				{ SKAdNetworkIdentifier = "av6w8kgt66.skadnetwork" },
				{ SKAdNetworkIdentifier = "cj5566h2ga.skadnetwork" },
				{ SKAdNetworkIdentifier = "f38h382jlk.skadnetwork" },
				{ SKAdNetworkIdentifier = "s39g8k73mm.skadnetwork" },
				{ SKAdNetworkIdentifier = "v9wttpbfk9.skadnetwork" },
				{ SKAdNetworkIdentifier = "n38lu8286q.skadnetwork" },
				{ SKAdNetworkIdentifier = "cstr6suwn9.skadnetwork" },
				{ SKAdNetworkIdentifier = "su67r6k2v3.skadnetwork" },
				{ SKAdNetworkIdentifier = "n9x2a789qt.skadnetwork" },
				{ SKAdNetworkIdentifier = "kbd757ywx3.skadnetwork" },
				{ SKAdNetworkIdentifier = "uw77j35x4d.skadnetwork" },
				{ SKAdNetworkIdentifier = "3sh42y64q3.skadnetwork" },
				{ SKAdNetworkIdentifier = "5l3tpt7t6e.skadnetwork" },
				{ SKAdNetworkIdentifier = "mls7yz5dvl.skadnetwork" },
				{ SKAdNetworkIdentifier = "5a6flpkh64.skadnetwork" },
				{ SKAdNetworkIdentifier = "578prtvx9j.skadnetwork" },
				{ SKAdNetworkIdentifier = "f73kdq92p3.skadnetwork" },
				{ SKAdNetworkIdentifier = "8m87ys6875.skadnetwork" },
				{ SKAdNetworkIdentifier = "488r3q3dtq.skadnetwork" },
				{ SKAdNetworkIdentifier = "zmvfpc5aq8.skadnetwork" },
				{ SKAdNetworkIdentifier = "97r2b46745.skadnetwork" },
				{ SKAdNetworkIdentifier = "6xzpu9s2p8.skadnetwork" },
				{ SKAdNetworkIdentifier = "cg4yq2srnc.skadnetwork" },
				{ SKAdNetworkIdentifier = "ecpz2srf59.skadnetwork" },
				{ SKAdNetworkIdentifier = "238da6jt44.skadnetwork" },
				{ SKAdNetworkIdentifier = "22mmun2rn5.skadnetwork" },
				{ SKAdNetworkIdentifier = "lr83yxwka7.skadnetwork" },
				{ SKAdNetworkIdentifier = "24t9a8vw3c.skadnetwork" },
				{ SKAdNetworkIdentifier = "v79kvwwj4g.skadnetwork" },
				{ SKAdNetworkIdentifier = "424m5254lk.skadnetwork" },
				{ SKAdNetworkIdentifier = "44n7hlldy6.skadnetwork" },
				{ SKAdNetworkIdentifier = "4dzt52r2t5.skadnetwork" },
				{ SKAdNetworkIdentifier = "wzmmz9fp6w.skadnetwork" },
				{ SKAdNetworkIdentifier = "bvpn9ufa9b.skadnetwork" },
				{ SKAdNetworkIdentifier = "gta9lk7p23.skadnetwork" },
			},
		},
	},
	android =
	{
		minSdkVersion = "16",
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

		-- All types
		['plugin.appodeal.Bidmachine'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.GoogleAdMob'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.A4G'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.AppLovin'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.FacebookAudience'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Smaato'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.StartApp'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Unity'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Yandex'] = { publisherId = 'com.coronalabs' },

		-- Banner
		['plugin.appodeal.AmazonAds'] = { publisherId = 'com.coronalabs' },

		-- Interstitial
		['plugin.appodeal.AdColony'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.AmazonAds'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.IronSource'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Ogury'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Vungle'] = { publisherId = 'com.coronalabs' },

		-- Rewarded Video
		['plugin.appodeal.AdColony'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.IronSource'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Ogury'] = { publisherId = 'com.coronalabs' },
		['plugin.appodeal.Vungle'] = { publisherId = 'com.coronalabs' },
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
['plugin.appodeal.Flurry'] = { publisherId = 'com.coronalabs' },
['plugin.appodeal.InMobi'] = { publisherId = 'com.coronalabs' },
-- ['plugin.appodeal.MyTarget'] = { publisherId = 'com.coronalabs' },
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

<!-- 
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

Please keep in mind, that using beta versions of both Appodeal SDK and CORONA_CORE_PRODUCT Appodeal plugin may cause unexpected issues. We've made a profound tests of a new system, but you should use it at your own risk.

</div>
-->

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

## Sample project

* [View on GitHub](https://github.com/coronalabs/plugins-sample-appodeal)
