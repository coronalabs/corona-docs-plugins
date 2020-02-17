# gpgs.videos.setListener()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.videos.*][plugin.gpgs-v2.videos]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Register a listener to listen for changes to the overlay state launched by [show][plugin.gpgs-v2.videos.show].

Note that only one request listener may be active at a time. Calling this method while another request listener was previously registered will replace the original listener with the new one.

## Syntax

	gpgs.videos.setListener(listener)

##### listener ~^(required)^~
_[Listener][api.type.Listener]._ Receives [video][plugin.gpgs-v2.videos.event.video] event.