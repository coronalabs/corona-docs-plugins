# gpgs.multiplayer.realtime.getRoom()

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

Returns a [Room][plugin.gpgs-v2.multiplayer.type.Room] object. To use this method the specified room must be created or joined to before that.

## Syntax

	gpgs.multiplayer.realtime.getRoom(roomId)

##### roomId ~^(required)^~
_[String][api.type.String]._ Room to retrive.