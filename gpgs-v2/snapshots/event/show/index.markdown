# show

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Event][api.type.Event]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.snapshots.*][plugin.gpgs-v2.snapshots]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Indicates that the snapshot view was cancelled or a specific snapshot was selected.

## Gotchas

`event.isError` could be `true` because the view was `"cancelled"`, that's not an error per se, but for consistency it is treated as an error.

## Properties

#### [event.name][plugin.gpgs-v2.snapshots.event.show.name]

#### [event.isError][plugin.gpgs-v2.snapshots.event.show.isError]

#### [event.errorMessage][plugin.gpgs-v2.snapshots.event.show.errorMessage]

#### [event.errorCode][plugin.gpgs-v2.snapshots.event.show.errorCode]

#### [event.snapshot][plugin.gpgs-v2.snapshots.event.show.snapshot]

#### [event.isNew][plugin.gpgs-v2.snapshots.event.show.isNew]