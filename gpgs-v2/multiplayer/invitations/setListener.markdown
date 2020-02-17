# gpgs.multiplayer.invitations.setListener()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.multiplayer.*][plugin.gpgs-v2.multiplayer]
>                       [gpgs-v2.multiplayer.invitations.*][plugin.gpgs-v2.multiplayer.invitations]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Register a listener to intercept incoming invitations for the currently signed-in user. If a listener is registered by this method, the incoming invitation will not generate a status bar notification as long as this client remains connected.

Note that only one invitation listener may be active at a time. Calling this method while another invitation listener was previously registered will replace the original listener with the new one.

## Syntax

	gpgs.multiplayer.invitations.setListener(listener)

##### listener ~^(required)^~
_[Listener][api.type.Listener]._ Receives [invitation][plugin.gpgs-v2.multiplayer.invitations.event.invitation] event.