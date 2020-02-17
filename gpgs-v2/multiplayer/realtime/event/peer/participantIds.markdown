# event.participantIds

> --------------------- ------------------------------------------------------------------------------------------
> __Event__             [peer][multiplayer.realtime.event.peer]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.realtime.*][plugin.gpgs-v2.multiplayer.realtime]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

_[Array][api.type.Array]._ Has [string][api.type.String] elements. The list of affected participants. Only available for phases `"peer declined"`, `"peer invited to room"`, `"peer joined"`, `"peer left"`, `"peers connected"`, `"peers disconnected"`.