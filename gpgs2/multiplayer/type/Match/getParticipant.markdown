# object.getParticipant()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      [Table][api.type.Table]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.multiplayer.*][plugin.gpgs2.multiplayer]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Returns Table - the [Participant][plugin.gpgs2.multiplayer.type.Participant] object for the specificied participant id. Or `nil` if not found.

## Syntax

	object.getParticipant(participantId)

##### participantId ~^(optional)^~
_[String][api.type.String]._ The id of the participant.