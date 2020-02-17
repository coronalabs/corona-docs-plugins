# gpgs.init()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Initializes the plugin. Calls the listener to notify when this process is done or to provide an error information.

## Syntax

	gpgs.init(listener)

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [init][plugin.gpgs-v2.event.init] event.