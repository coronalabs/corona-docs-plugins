# gpgs.multiplayer.turnbased.create()

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

Create a new turn-based match for the current game. If the provided automatch parameters, the server will attempt to find any previously created matches that satisfy these parameters and join the current player into the previous match. If no suitable match can be found, a new match will be created.

## Syntax

	gpgs.multiplayer.turnbased.create(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### playerId ~^(optional)^~
_[String][api.type.String]._ Invites only this player.

##### playerIds ~^(optional)^~
_[Array][api.type.Array]._ Populate with [string][api.type.String] elements. If provided invites all specified players. Higher priority thann `playerId`.

##### automatch ~^(optional)^~
_[Table][api.type.Table]._ Specifies automatch options.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [create][plugin.gpgs2.multiplayer.turnbased.event.create] event.

## automatch Table Parameters

##### minPlayers ~^(optional)^~
_[Integer][api.type.Integer]._ Minimum number of auto-matched players.

##### maxPlayers ~^(optional)^~
_[Integer][api.type.Integer]._ Maximum number of auto-matched players.

##### exclusionBits ~^(optional)^~
_[Integer][api.type.Integer]._ Exclusive bitmasks for the automatching request. The logical AND of each pairing of automatching requests must equal zero for auto-match.

##### variant ~^(optional)^~
_[Integer][api.type.Integer]._ This is an optional, developer-controlled parameter describing the type of game to play, and is used for auto-matching criteria. Must be a positive integer.