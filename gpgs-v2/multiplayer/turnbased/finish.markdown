# gpgs.multiplayer.turnbased.finish()

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

Indicates that a participant is finished with a match. Optionally sends match results to specified participants.

## Syntax

	gpgs.multiplayer.turnbased.finish(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### matchId ~^(required)^~
_[String][api.type.String]._ Multiplayer match id.

##### payload ~^(optional)^~
_[String][api.type.String]._ Match data to send to other participants. It has a size limit, see [getLimits][plugin.gpgs-v2.multiplayer.getLimits].

##### results ~^(optional)^~
_[Array][api.type.Array]._ Populate with result table elements. The client which calls `finish` is responsible for reporting the results for all appropriate participants in the match. Not every participant is required to have a result, but providing results for participants who are not in the match is an error.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [finish][plugin.gpgs-v2.multiplayer.turnbased.event.finish] event.

## Results Table Reference

##### participantId ~^(required)^~
_[String][api.type.String]._ Participant to send the result to.

##### result ~^(optional)^~
_[String][api.type.String]._ The result of the match. One of , `"disagreed"`, `"disconnect"`, `"loss"`, `"tie"`, `"win"`, `"none"`. Default is `"none"`.

##### placing ~^(optional)^~
_[Integer][api.type.Integer]._ The place the participant has earned.