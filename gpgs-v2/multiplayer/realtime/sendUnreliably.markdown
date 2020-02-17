# gpgs.multiplayer.realtime.sendUnreliably()

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

Sends a message to a participant in a real-time room reliably. The caller will receive a callback to report the status of the send message operation.

## Syntax

	gpgs.multiplayer.realtime.sendUnreliably(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### roomId ~^(required)^~
_[String][api.type.String]._ Multiplayer room id.

##### participantId ~^(optional)^~
_[String][api.type.String]._ Participant to send the message to.

##### participantIds ~^(optional)^~
_[Array][api.type.Array]._ Populate with [string][api.type.String] elements. If provided sends the message to the specified participants. Higher priority than `participantId`.

##### payload ~^(required)^~
_[String][api.type.String]._ Message to send. It has a size limit, see [getLimits][plugin.gpgs-v2.multiplayer.getLimits].