# Google Play Games Services

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.library]
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
				supportedPlatforms = {["android"] = true, ["android-kindle"] = true}
			}
		}
	}

## Nodes

The plugin is divided into API nodes for better organization.

#### [gpgs-v2.achievements][plugin.gpgs-v2.achievements]

#### [gpgs-v2.leaderboards][plugin.gpgs-v2.leaderboards]

#### [gpgs-v2.players][plugin.gpgs-v2.players]

#### [gpgs-v2.events][plugin.gpgs-v2.events]

#### [gpgs-v2.snapshots][plugin.gpgs-v2.snapshots]

#### [gpgs-v2.videos][plugin.gpgs-v2.videos]

#### [gpgs-v2.multiplayer][plugin.gpgs-v2.multiplayer]

#### [gpgs-v2.multiplayer.invitations][plugin.gpgs-v2.multiplayer.invitations]

#### [gpgs-v2.multiplayer.realtime][plugin.gpgs-v2.multiplayer.realtime]

#### [gpgs-v2.multiplayer.turnbased][plugin.gpgs-v2.multiplayer.turnbased]

## gpgs.*

## Overview

This is the base API node for the plugin. It manages connection to the Google's servers, authentication and general SDK tasks.

## Functions

#### [gpgs-v2.enableDebug()][plugin.gpgs-v2.enableDebug]

#### [gpgs-v2.init(listener)][plugin.gpgs-v2.init]

#### [gpgs-v2.isConnected()][plugin.gpgs-v2.isConnected]

#### [gpgs-v2.login(params)][plugin.gpgs-v2.login]

#### [gpgs-v2.logout()][plugin.gpgs-v2.logout]

#### [gpgs-v2.getAccountName(listener)][plugin.gpgs-v2.getAccountName]

#### [gpgs-v2.getServerAuthCode(params)][plugin.gpgs-v2.getServerAuthCode]

#### [gpgs-v2.setPopupPosition(position)][plugin.gpgs-v2.setPopupPosition]

#### [gpgs-v2.loadGame(listener)][plugin.gpgs-v2.loadGame]

#### [gpgs-v2.clearNotifications(notificationTypes)][plugin.gpgs-v2.clearNotifications]

#### [gpgs-v2.loadImage(params)][plugin.gpgs-v2.loadImage]

#### [gpgs-v2.showSettings(listener)][plugin.gpgs-v2.showSettings]

## Events

#### [init][plugin.gpgs-v2.event.init]

#### [login][plugin.gpgs-v2.event.login]

#### [getAccountName][plugin.gpgs-v2.event.getAccountName]

#### [getServerAuthCode][plugin.gpgs-v2.event.getServerAuthCode]

#### [loadGame][plugin.gpgs-v2.event.loadGame]

#### [loadImage][plugin.gpgs-v2.event.loadImage]

## Types

#### [Game][plugin.gpgs-v2.type.Game]
