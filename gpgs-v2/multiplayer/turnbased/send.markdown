# gpgs.multiplayer.turnbased.send()

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

Indicates that a participant is finished his turn. Optionally sends match results to specified participants. Must indicate who will take the next turn.

## Syntax

	gpgs.multiplayer.turnbased.send(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### matchId ~^(required)^~
_[String][api.type.String]._ Multiplayer match id.

##### pendingParticipantId ~^(optional)^~
_[String][api.type.String]._ Participant that will have the next turn.

##### isPendingAutomatch ~^(optional)^~
_[Boolean][api.type.Boolean]._ Whether to wait for additional automatched players to take the next turn (if possible).

##### payload ~^(optional)^~
_[String][api.type.String]._ Match data to send to other participants. It has a size limit, see [getLimits][plugin.gpgs-v2.multiplayer.getLimits].

##### results ~^(optional)^~
_[Array][api.type.Array]._ Populate with result table elements. Optional list of results for this match. Note that the results reported here should be final - if results reported later conflict with these values, the returned value will indicate a conflicted result. This is most useful for cases where a participant knows their results early. For example, a single elimination game where participants are eliminated as the game continues might wish to specify results for the eliminated participants here.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [send][plugin.gpgs-v2.multiplayer.turnbased.event.send] event.

## Results Table Reference

##### participantId ~^(required)^~
_[String][api.type.String]._ Participant to send the result to.

##### result ~^(optional)^~
_[String][api.type.String]._ The result of the match. One of , `"disagreed"`, `"disconnect"`, `"loss"`, `"tie"`, `"win"`, `"none"`. Default is `"none"`.

##### placing ~^(optional)^~
_[Integer][api.type.Integer]._ The place the participant has earned.