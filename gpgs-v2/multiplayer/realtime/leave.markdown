# gpgs.multiplayer.realtime.leave()

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

Leave the specified room. This will disconnect the player from the room, but allow other players to continue playing the game. The result is delivered to the `"room"` listener defined using [setListeners][plugin.gpgs-v2.multiplayer.realtime.setListeners].

After this method is called, you cannot perform any further actions on the room. You can create or join another room only after the correspoding `"room"` is received.

## Syntax

	gpgs.multiplayer.realtime.leave(roomId)

##### roomId ~^(required)^~
_[String][api.type.String]._ Room to leave.