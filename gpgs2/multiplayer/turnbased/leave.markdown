# gpgs.multiplayer.turnbased.leave()

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

Leaves a match. If it's currently the players turn, must provide the participant id who has the next turn or specifiy that the match needs another automatch participant.

## Syntax

	gpgs.multiplayer.turnbased.leave(matchId)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### matchId ~^(required)^~
_[String][api.type.String]._ Match to leave.

##### pendingParticipantId ~^(optional)^~
_[String][api.type.String]._ Participant that will have the next turn.

##### isPendingAutomatch ~^(optional)^~
_[Boolean][api.type.Boolean]._ Whether to wait for additional automatched players to take the next turn (if possible).

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [leave][plugin.gpgs2.multiplayer.turnbased.event.leave] event.