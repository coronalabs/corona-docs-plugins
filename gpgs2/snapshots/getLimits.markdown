# gpgs.snapshots.getLimits()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Integer][api.type.Integer]
> __Return value__      [Table][api.type.Table]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.snapshots.*][plugin.gpgs2.snapshots]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Retrieves various limits associated with the Snapshots API.

## Syntax

	gpgs.snapshots.getLimits()

Returns Table. See the next section for details. Can be `nil` if service is unavailable.

## Return Table Reference

##### imageSize
_[Integer][api.type.Integer]._ The maximum data size per snapshot cover image in bytes. Guaranteed to be at least 800 KB. May increase in the future.
##### payloadSize
_[Integer][api.type.Integer]._ The maximum data size per snapshot in bytes. Guaranteed to be at least 3 MB. May increase in the future.