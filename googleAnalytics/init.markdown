# googleAnalytics.init()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          analytics, Google Analytics, googleAnalytics, init
> __See also__          [googleAnalytics.logEvent()][plugin.googleAnalytics.logEvent]
>						[googleAnalytics.logScreenName()][plugin.googleAnalytics.logScreenName]
>						[googleAnalytics.*][plugin.googleAnalytics]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Initalizes the Google Analytics plugin. This step is mandatory before any other features or methods can be used.


## Syntax

	googleAnalytics.init( )


## Example

``````lua
local googleAnalytics = require( "plugin.googleAnalytics" )

-- Initialize Google Analytics
googleAnalytics.init( )
``````
