# admob.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, AdMob
> __Platforms__			Android, iOS
> __Sample__			[https://github.com/coronalabs/plugins-sample-admob](https://github.com/coronalabs/plugins-sample-admob)
> --------------------- ------------------------------------------------------------------------------------------


## Overview

The AdMob plugin allows developers to monetize users through AdMob static interstitial ads, video interstitial ads, rewarded video ads, and banner ads.

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

Check out new `hasUserConsent`  [admob.load()][plugin.admob.load] parameter to enable GDPR data collection restrictions.

</div>


## Registration

Before you can use this plugin, you must [register](https://www.google.com/admob/) with AdMob.


## Syntax

	local admob = require( "plugin.admob" )


## Functions

#### [admob.init()][plugin.admob.init]

#### [admob.load()][plugin.admob.load]

#### [admob.isLoaded()][plugin.admob.isLoaded]

#### [admob.show()][plugin.admob.show]

#### [admob.hide()][plugin.admob.hide]

#### [admob.height()][plugin.admob.height]

#### [admob.setVideoAdVolume()][plugin.admob.setVideoAdVolume]


## Events

#### [adsRequest][plugin.admob.event.adsRequest]


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````{ brush="lua" gutter="false" first-line="1" highlight="[5,6,7,8,9,10,11,16,17,18,19,24,25,26,27]" }
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
	
	iphone = 
	{
		plist = 
		{
			 GADApplicationIdentifier = "[YOUR_ADMOB_APP_ID]",  -- replace with your app id. https://developers.google.com/admob/ios/quick-start#update_your_infoplist
		},
	},
	
	plugins =
	{
		["plugin.admob"] =
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

</div>
