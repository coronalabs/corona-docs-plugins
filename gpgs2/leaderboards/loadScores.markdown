# gpgs.leaderboards.loadScores()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.leaderboards.*][plugin.gpgs2.leaderboards]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Retrieves scores from a specified leaderboard.

## Syntax

	gpgs.leaderboards.loadScores(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### leaderboardId ~^(required)^~
_[String][api.type.String]._ Leaderboard id from which to load scores.

##### position ~^(optional)^~
_[String][api.type.String]._ Can be one of these: `"single"` - current player score, `"top"` - top scores, `"centered"` - scores around current player score. Default is `"top"`.

##### friendsOnly ~^(optional)^~
_[Boolean][api.type.Boolean]._ If true - load only scores for the current player's friends.

##### limit ~^(optional)^~
_[Integer][api.type.Integer]._ How many scores to load, max and default is 25.

##### timeSpan ~^(optional)^~
_[String][api.type.String]._ Can be one of these: `"all time"`, `"weekly"` - scores are reset each week, `"daily"` - scores are reset daily. Default is `"all time"`.

##### reload ~^(optional)^~
_[Boolean][api.type.Boolean]._ If `true`, the data will be pulled fresh, not from a cache.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [loadScores][plugin.gpgs2.leaderboards.event.loadScores] event.