# gpgs.multiplayer.turnbased.join()

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

Joins a match.

## Syntax

	gpgs.multiplayer.turnbased.join(invitationId)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### invitationId ~^(required)^~
_[String][api.type.String]._ Invitation to accept and join the associated match.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [join][plugin.gpgs2.multiplayer.turnbased.event.join] event.