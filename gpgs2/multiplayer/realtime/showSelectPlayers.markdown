# gpgs.multiplayer.realtime.showSelectPlayers()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.multiplayer.*][plugin.gpgs2.multiplayer]
>                       [gpgs2.multiplayer.realtime.*][plugin.gpgs2.multiplayer.realtime]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Shows a view that will let the user select players to send an invitation to for a real-time multiplayer match.

The number of players passed in should be the desired number of additional players to select, not including the current player. So, for a game that can handle between 2 and 4 players, `minPlayers` would be 1 and `maxPlayers` would be 3.

## Syntax

	gpgs.multiplayer.realtime.showSelectPlayers(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### playerId ~^(optional)^~
_[String][api.type.String]._ Preselect this player.

##### playerIds ~^(optional)^~
_[Array][api.type.Array]._ Populate with [string][api.type.String] elements. Preselect these players. Higher priority than `playerId`.

##### minPlayers ~^(optional)^~
_[Integer][api.type.Number]._ The minimum number of players to select (not including the current player).

##### maxPlayers ~^(optional)^~
_[Integer][api.type.Number]._ The maximum number of players to select (not including the current player).

##### allowAutomatch ~^(optional)^~
_[Boolean][api.type.Boolean]._ Whether or not to display an option for selecting automatch players.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [showSelectPlayers][plugin.gpgs2.multiplayer.realtime.event.showSelectPlayers] event.