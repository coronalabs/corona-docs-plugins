# gpgs.multiplayer.realtime.join()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.realtime.*][plugin.gpgs-v2.multiplayer.realtime]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Join a real-time room by accepting an invitation. The lifetime of the current game's connection to the room is bound to this client's lifecycle. When the client disconnects, the player will leave the room and any peer-to-peer connections for this player will be torn down. The result is delivered to the `"room"` listener defined using [setListeners][plugin.gpgs-v2.multiplayer.realtime.setListeners].

## Syntax

	gpgs.multiplayer.realtime.join(invitationId)

##### invitationId ~^(required)^~
_[String][api.type.String]._ Invitation to accept and join the associated room.