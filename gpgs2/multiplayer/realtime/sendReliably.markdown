# gpgs.multiplayer.realtime.sendReliably()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs2.multiplayer.*][plugin.gpgs2.multiplayer]
>                       [gpgs2.multiplayer.realtime.*][plugin.gpgs2.multiplayer.realtime]
>                       [gpgs2.*][plugin.gpgs2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Sends a message to participants in a real-time room reliably. The caller will receive callbacks to report the status of the send message operation for each participant.

## Syntax

	gpgs.multiplayer.realtime.sendReliably(params)

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
_[String][api.type.String]._ Message to send. It has a size limit, see [getLimits][plugin.gpgs2.multiplayer.getLimits].

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [sendReliably][plugin.gpgs2.multiplayer.realtime.event.sendReliably] event.