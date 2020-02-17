# gpgs.multiplayer.turnbased.load()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.multiplayer.*][plugin.gpgs2.multiplayer]
>                       [gpgs2.multiplayer.turnbased.*][plugin.gpgs2.multiplayer.turnbased]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Retrieves information on all turnbased matches for the current player.

## Syntax

	gpgs.multiplayer.turnbased.load(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### matchId ~^(optional)^~
_[String][api.type.String]._ If provided loads only this match information. If not - loads information on all matches.

##### filters ~^(optional)^~
_[Array][api.type.Array]._ Populate with [string][api.type.String] elements. If provided selects only specified turn states of matches. Elements of that table can be: `"complete"`, `"invited"`, `"my turn"`, `"their turn"`.

##### mostRecentFirst ~^(optional)^~
_[Boolean][api.type.Boolean]._ If `true`, the results will be sorted by date. By default the results are sorted in social order.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [load][plugin.gpgs2.multiplayer.turnbased.event.load] event.