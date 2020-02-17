# gpgs.players.showCompare()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.players.*][plugin.gpgs2.players]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Shows a view to compare the current player with a specified one.

## Syntax

	gpgs.players.showCompare(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### playerId ~^(required)^~
_[String][api.type.String]._ Player to compare with.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [showCompare][plugin.gpgs2.players.event.showCompare] event.