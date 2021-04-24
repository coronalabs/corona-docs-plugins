# gpgs.multiplayer.realtime.show()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.realtime.*][plugin.gpgs-v2.multiplayer.realtime]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Shows a view that will display a "waiting room" screen that shows the progress of participants joining a real-time multiplayer room.

## Syntax

	gpgs.multiplayer.realtime.show(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### roomId ~^(optional)^~
_[String][api.type.String]._ The multiplayer room id.

##### minPlayersRequired ~^(optional)^~
_[Integer][api.type.Number]._ If desired, the waiting room can allow the user to start playing the game even before the room is fully connected. This is controlled by the `minPlayersRequired` parameter: if at least that many participants (including the current player) are connected to the room, a "Start playing" menu item will become enabled in the waiting room UI. Setting `minPlayersRequired` to 0 means that "Start playing" will always be available, and a value of MAX_VALUE will disable the item completely. Note: if you do allow the user to start early, you'll need to handle that situation by explicitly telling the other connected peers that the game is now starting; see the developer documentation for more details.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [show][plugin.gpgs-v2.multiplayer.realtime.event.show] event.