# gpgs.multiplayer.invitations.load()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Boolean][api.type.Boolean]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.invitations.*][plugin.gpgs-v2.multiplayer.invitations]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Retrieves information on all invitations for the current player.

## Syntax

	gpgs.multiplayer.invitations.load(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### mostRecentFirst ~^(optional)^~
_[Boolean][api.type.Boolean]._ If `true`, the results will be sorted by date. By default the results are sorted in social order.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [load][plugin.gpgs-v2.multiplayer.invitations.event.load] event.