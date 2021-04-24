# gpgs.multiplayer.realtime.create()

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

Creates a real-time room for the current game. The lifetime of the current game's connection to the room is bound to this client's lifecycle. When the client disconnects, the player will leave the room and any peer-to-peer connections for this player will be torn down. The result is delivered to the `"room"` listener defined using [setListeners][plugin.gpgs-v2.multiplayer.realtime.setListeners].

## Syntax

	gpgs.multiplayer.realtime.create(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### playerId ~^(optional)^~
_[String][api.type.String]._ Invites only this player.

##### playerIds ~^(optional)^~
_[Array][api.type.Array]._ Populate with [string][api.type.String] elements. If provided invites all specified players. Higher priority thann `playerId`.

##### automatch ~^(optional)^~
_[Table][api.type.Table]._ Specifies automatch options.

## automatch Table Parameters

##### minPlayers ~^(optional)^~
_[Integer][api.type.Number]._ Minimum number of auto-matched players.

##### maxPlayers ~^(optional)^~
_[Integer][api.type.Number]._ Maximum number of auto-matched players.

##### exclusionBits ~^(optional)^~
_[Integer][api.type.Number]._ Exclusive bitmasks for the automatching request. The logical AND of each pairing of automatching requests must equal zero for auto-match.

##### variant ~^(optional)^~
_[Integer][api.type.Number]._ This is an optional, developer-controlled parameter describing the type of game to play, and is used for auto-matching criteria. Must be a positive integer.