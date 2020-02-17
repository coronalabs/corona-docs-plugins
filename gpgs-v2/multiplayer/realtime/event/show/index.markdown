# show

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Event][api.type.Event]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.realtime.*][plugin.gpgs-v2.multiplayer.realtime]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Indicates that the waiting room view was closed.

## Gotchas

`event.isError` will be `true` because the view was `"cancelled"`, that's not an error per se, but for consistency it is treated as an error.

## Properties

#### [event.name][plugin.gpgs-v2.multiplayer.realtime.event.show.name]

#### [event.isError][plugin.gpgs-v2.multiplayer.realtime.event.show.isError]

#### [event.errorMessage][plugin.gpgs-v2.multiplayer.realtime.event.show.errorMessage]

#### [event.errorCode][plugin.gpgs-v2.multiplayer.realtime.event.show.errorCode]