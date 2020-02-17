# gpgs.multiplayer.realtime.setListeners()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Table][api.type.Table]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.realtime.*][plugin.gpgs-v2.multiplayer.realtime]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Register listeners to intercept incoming messages for the multiplayer room. Track peer statuses and room state.

Note that only one listener of each kind may be active at a time. Calling this method while another listener of a kind was previously registered will replace the original listener with the new one.

## Syntax

	gpgs.multiplayer.realtime.setListeners(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### message ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [message][plugin.gpgs-v2.multiplayer.realtime.event.message] event.

##### peer ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [peer][plugin.gpgs-v2.multiplayer.realtime.event.peer] event.

##### room ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [room][plugin.gpgs-v2.multiplayer.realtime.event.room] event.