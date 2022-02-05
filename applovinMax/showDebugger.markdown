# applovinMax.showDebugger()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__				[Function][api.type.Function]
> __Return value__		[Boolean][api.type.Boolean]
> __Revision__			[REVISION_LABEL](REVISION_URL)
> __Keywords__			ads, advertising, AppLovin, showDebugger, AppLovin Max
> __See also__			[applovinMax.show()][plugin.applovinMax.show]
>						[applovinMax.*][plugin.applovinMax]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Will show a pop up on iOS and Android that show mediation integration, SDK versions, load test ads, and more info about your AppLovin Setup.


## Syntax

	applovinMax.showDebugger()


## Example

``````lua
local applovinMax = require( "plugin.applovinMax" )

local function adListener( event )

	if ( event.phase == "init" ) then  -- Successful initialization
		print( event.isError )
		-- Load an AppLovin ad
		applovinMax.load( "interstitial",  {iOSUnitId ="replace with your own", androidUnitId="replace with your own"} )

	elseif ( event.phase == "loaded" ) then  -- The ad was successfully loaded
		print( event.type )

	elseif ( event.phase == "failed" ) then  -- The ad failed to load
		print( event.type )
		print( event.isError )
		print( event.response )
	end
end

-- Initialize the AppLovin plugin
applovinMax.init( adListener )

-- After Init, show the debugger pop up
applovinMax.showDebugger()
``````
