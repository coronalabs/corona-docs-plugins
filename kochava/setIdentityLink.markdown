# kochava.setIdentityLink()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__		none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          analytics, attribution, Kochava, setIdentityLink
> __See also__			[kochava.*][plugin.kochava]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Links the Kochava device ID with user-defined identities. This provides you the opportunity to link different identities together. For example, you may have assigned each user of your app an internal user&nbsp;ID which you want to connect to a user's service identifier. Using this method, you can send both your internal user&nbsp;ID and their service identifier and connect them in the Kochava database.

<div class="guide-notebox">
<div class="notebox-title">Note</div>

A maximum of two key-value pairs can be set with each call.

</div>


## Syntax

	kochava.setIdentityLink( linkTable )

##### linkTable ~^(required)^~
_[Table][api.type.Table]._ A table containing key-value pairs.


## Example

``````lua
local kochava = require( "plugin.kochava" )

local function kochavaListener( event )
	-- Handle events here
end

-- Initialize plugin
kochava.init( kochavaListener,
	{
		appGUID = "YOUR_APP_GUID"
	}
)

kochava.setIdentityLink( { myInternalUserID="12345" } )
``````
