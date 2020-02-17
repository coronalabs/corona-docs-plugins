# gpgs.multiplayer.turnbased.getMatch()

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

Returns a [Match][plugin.gpgs-v2.multiplayer.type.Match] object. To use this method the specified match must be created, loaded or joined to before that.

## Syntax

	gpgs.multiplayer.turnbased.getMatch(matchId)

##### matchId ~^(required)^~
_[String][api.type.String]._ Match to retrive.