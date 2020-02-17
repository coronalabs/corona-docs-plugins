# gpgs.multiplayer.turnbased.cancel()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.turnbased.*][plugin.gpgs-v2.multiplayer.turnbased]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Cancels a match.

## Syntax

	gpgs.multiplayer.turnbased.cancel(matchId)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### matchId ~^(required)^~
_[String][api.type.String]._ Match to cancel.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [cancel][plugin.gpgs-v2.multiplayer.turnbased.event.cancel] event.