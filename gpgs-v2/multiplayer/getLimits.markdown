# gpgs.multiplayer.getLimits()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Integer][api.type.Integer]
> __Return value__      [Table][api.type.Table]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Retrieves various limits associated with the Multiplayer API.

## Syntax

	gpgs.multiplayer.getLimits()

Returns Table. See the next section for details. Can be `nil` if service is unavailable.

## Return Table Reference

##### reliablePayloadSize
_[Integer][api.type.Integer]._ The maximum message size supported by reliable send in realtime multiplayer.

##### unreliablePayloadSize
_[Integer][api.type.Integer]._ The maximum message size supported by unreliable send in realtime multiplayer.

##### matchPayloadSize
_[Integer][api.type.Integer]._ The maximum data size per match in bytes. Guaranteed to be at least 128 KB. May increase in the future.