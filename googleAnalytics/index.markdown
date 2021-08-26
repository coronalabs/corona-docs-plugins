# googleAnalytics.* &mdash; Google Analytics

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          analytics, Google Analytics, googleAnalytics
> __Platforms__			Android, iOS
> __Sample__			[https://github.com/coronalabs/plugins-sample-googleAnalytics](https://github.com/coronalabs/plugins-sample-googleAnalytics)
> --------------------- ------------------------------------------------------------------------------------------


## Overview

The Google Analytics plugin lets you measure the value of your app across all stages, discover what keeps users engaged, and learn how to make your app more successful.

<div class="guide-notebox-imp">
<div class="notebox-title-imp">Important</div>

* Stating with Solar2D 2021.3652+, Google Analytics will be using Firebase


## Registration

Before implementing the Google Analytics plugin, you must [setup a Firebase Project](https://console.firebase.google.com) and add __google-services.json__ for Android and/or add __GoogleService-Info.plist__ for iOS, provided in the Firebase console, to project settings to your Solar2D project's root directory alongside `main.lua`.


## Syntax

	local googleAnalytics = require( "plugin.googleAnalytics" )


## Functions

#### [googleAnalytics.init()][plugin.googleAnalytics.init]

#### [googleAnalytics.logEvent()][plugin.googleAnalytics.logEvent]

#### [googleAnalytics.logScreenName()][plugin.googleAnalytics.logScreenName]


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````lua
settings =
{
	android =
	{
				useGoogleServicesJson = true, -- Needed for Android
	},
	plugins =
	{
		["plugin.googleAnalytics"] =
		{
			publisherId = "com.coronalabs"
		},
	},		
}
``````

<div class="guide-notebox">
<div class="notebox-title">Note</div>

For Android, the following permissions/features are automatically added when using this plugin:

* `"android.permission.INTERNET"`
* `"android.permission.ACCESS_NETWORK_STATE"`
* `"android.permission.WAKE_LOCK"`


</div>


## Support

* [https://analytics.google.com/](https://analytics.google.com/)
* [Solar2D Forums](https://forums.solar2d.com/c/corona-marketplace/13)
