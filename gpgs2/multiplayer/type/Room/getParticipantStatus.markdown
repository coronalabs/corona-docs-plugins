# object.getParticipantStatus()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      [String][api.type.String]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.multiplayer.*][plugin.gpgs2.multiplayer]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Returns String - the status of a participant or `nil` if not found. Can be one of these: `"invited"`, `"joined"`, `"declined"`, `"left"`.

## Syntax

	object.getParticipantStatus(participantId)

##### participantId ~^(optional)^~
_[String][api.type.String]._ The id of the participant.