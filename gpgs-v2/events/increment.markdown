# gpgs.events.increment()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.events.*][plugin.gpgs-v2.events]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Increments an event value.

## Syntax

	gpgs.events.increment(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### eventId ~^(required)^~
_[String][api.type.String]._ Event to increment.

##### steps ~^(optional)^~
_[Integer][api.type.Number]._ Incremental value. Default is 1.