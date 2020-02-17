# gpgs.leaderboards.submit()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.leaderboards.*][plugin.gpgs-v2.leaderboards]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Submits score to a leaderboard.

## Syntax

	gpgs.leaderboards.submit(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### leaderboardId ~^(required)^~
_[String][api.type.String]._ Leaderboard id to submit to.

##### score ~^(required)^~
Number. Score value.

##### tag ~^(optional)^~
_[String][api.type.String]._ Optional extra info, must be URL safe, max size is 64 bytes.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [submit][plugin.gpgs-v2.leaderboards.event.submit] event.