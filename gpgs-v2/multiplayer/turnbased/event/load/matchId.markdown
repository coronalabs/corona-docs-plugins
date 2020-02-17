# event.matchId

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Event__             [load][multiplayer.turnbased.event.load]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.turnbased.*][plugin.gpgs-v2.multiplayer.turnbased]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

_[String][api.type.String]._ Id of the match that was just loaded. You can now use [getMatch][plugin.gpgs-v2.multiplayer.turnbased.getMatch] to get it's object. Only available if `matchId` was specified in the call.