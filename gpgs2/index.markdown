# Google Play Games Services

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          google, google play games services, achievements, leaderboards, multiplayer
> __Platforms__         Android
> __Sample__            [https://github.com/coronalabs/com.coronalabs-plugin.gpgs.v2](https://github.com/coronalabs/com.coronalabs-plugin.gpgs.v2/tree/master/src/Corona)
> --------------------- ------------------------------------------------------------------------------------------

## Beta version

This plugin is currently in beta. API may change without notice.
iOS version will be available later.

## Overview

This plugin enables access to Google Play Games Services API, such as achievements, leaderboards and multiplayer.

## Backward compatipility

This plugin has full backward compatibility with the `gameNetwork.*` API. To use it, however, you have to require `"plugin.gpgs.v2"` before using `gameNetwork`.

## Syntax

	local gpgs = require( "plugin.gpgs.v2" )

## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

	settings = {
		plugins = {
			["plugin.gpgs.v2"] = {
				publisherId = "com.coronalabs",
				supportedPlatforms = { ["android"] = true }
			}
		}
	}

Additionally, you must specify the <nobr>Google Play Games App ID</nobr> in the `android` table of `build.settings` as the `googlePlayGamesAppId` key:

``````{ brush="lua" gutter="false" first-line="1" highlight="[5]" }
settings = {

	android =
	{
		googlePlayGamesAppId = "YOUR_APPLICATION_ID",
	},
}
``````

## Nodes

The plugin is divided into API nodes for better organization.

#### [gpgs2.achievements][plugin.gpgs2.achievements]

#### [gpgs2.leaderboards][plugin.gpgs2.leaderboards]

#### [gpgs2.players][plugin.gpgs2.players]

#### [gpgs2.events][plugin.gpgs2.events]

#### [gpgs2.snapshots][plugin.gpgs2.snapshots]

#### [gpgs2.videos][plugin.gpgs2.videos]

#### [gpgs2.multiplayer][plugin.gpgs2.multiplayer]

#### [gpgs2.multiplayer.invitations][plugin.gpgs2.multiplayer.invitations]

#### [gpgs2.multiplayer.realtime][plugin.gpgs2.multiplayer.realtime]

#### [gpgs2.multiplayer.turnbased][plugin.gpgs2.multiplayer.turnbased]

## gpgs.*

## Overview

This is the base API node for the plugin. It manages connection to the Google's servers, authentication and general SDK tasks.

## Functions

#### [gpgs2.enableDebug()][plugin.gpgs2.enableDebug]

#### [gpgs2.isConnected()][plugin.gpgs2.isConnected]

#### [gpgs2.isAuthenticated()][plugin.gpgs2.isAuthenticated]

#### [gpgs2.login(params)][plugin.gpgs2.login]

#### [gpgs2.logout()][plugin.gpgs2.logout]

#### [gpgs2.getAccountName(listener)][plugin.gpgs2.getAccountName]

#### [gpgs2.getServerAuthCode(params)][plugin.gpgs2.getServerAuthCode]

#### [gpgs2.setPopupPosition(position)][plugin.gpgs2.setPopupPosition]

#### [gpgs2.loadGame(listener)][plugin.gpgs2.loadGame]

#### [gpgs2.clearNotifications(notificationTypes)][plugin.gpgs2.clearNotifications]

#### [gpgs2.loadImage(params)][plugin.gpgs2.loadImage]

#### [gpgs2.showSettings(listener)][plugin.gpgs2.showSettings]

## Events

#### [login][plugin.gpgs2.event.login]

#### [getAccountName][plugin.gpgs2.event.getAccountName]

#### [getServerAuthCode][plugin.gpgs2.event.getServerAuthCode]

#### [loadGame][plugin.gpgs2.event.loadGame]

#### [loadImage][plugin.gpgs2.event.loadImage]

## Types

#### [Game][plugin.gpgs2.type.Game]
