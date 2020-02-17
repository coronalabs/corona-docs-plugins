
# Apple Game Center

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Library][api.type.Library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          gameNetwork, Game Center
> __Platforms__			iOS
> __Sample__			[https://github.com/coronalabs/plugins-sample-gamenetwork-apple](https://github.com/coronalabs/plugins-sample-gamenetwork-apple)
> --------------------- ------------------------------------------------------------------------------------------

## Overview

[Game Center](https://developer.apple.com/game-center/) lets friends in on the action with leaderboards and achievements. The nomenclature used in the Corona APIs for Game Center attempt to match the official Game Center APIs as much as possible, allowing you to <nobr>cross-reference</nobr> with official Game Center documentation.

## Gotchas

Game Center is not supported in the Corona Simulator.

## Syntax

	local gameNetwork = require( "gameNetwork" )

## Functions

#### [gameNetwork.init()][plugin.gameNetwork-apple.init]

#### [gameNetwork.request()][plugin.gameNetwork-apple.request]

#### [gameNetwork.show()][plugin.gameNetwork-apple.show]

## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````lua
settings =
{
	plugins =
	{
		["CoronaProvider.gameNetwork.apple"] =
		{
			publisherId = "com.coronalabs"
		},
	},
}
``````
