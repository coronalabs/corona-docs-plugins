# gpgs.achievements.reveal()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.achievements.*][plugin.gpgs2.achievements]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Reveals a hidden achievement.

## Syntax

	gpgs.achievements.reveal(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### achievementId ~^(required)^~
_[String][api.type.String]._ Achievement to reveal.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [reveal][plugin.gpgs2.achievements.event.reveal] event.