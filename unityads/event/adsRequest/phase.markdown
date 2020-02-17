# event.phase

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Event__             [adsRequest][plugin.unityads.event.adsRequest]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          ads, advertising, Unity Ads, adsRequest, phase
> __See also__			[adsRequest][plugin.unityads.event.adsRequest]
>						[unityads.*][plugin.unityads]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

[String][api.type.String] value indicating the phase of the [adsRequest][plugin.unityads.event.adsRequest] event. Possible values include:

* `"init"` &mdash; Indicates that the Unity&nbsp;Ads plugin was initialized successfully. You must wait for this event phase before trying to show ads.

* `"loaded"` &mdash; Indicates that an ad has been loaded successfully.

* `"displayed"` &mdash; Indicates that an ad has been displayed successfully via [unityads.show()][plugin.unityads.show].

* `"skipped"` &mdash; Indicates that video ad playback was stopped by the user before the end of playback.

* `"completed"` &mdash; Indicates that the user viewed the video ad until its completion.
 
* `"failed"` &mdash; Indicates that an ad failed to load. For this phase, [event.isError][plugin.unityads.event.adsRequest.isError] will be `true` and [event.response][plugin.unityads.event.adsRequest.response] provides additional context on the error. Additionally, for this phase, [event.data][plugin.unityads.event.adsRequest.data] is a <nobr>JSON-formatted</nobr> string containing `errorCode` and `errorMsg` keys.

* `"placementStatus"` &mdash; This phase is triggered by a call to [unityads.isLoaded()][plugin.unityads.isLoaded]. In this case, [event.data][plugin.unityads.event.adsRequest.data] will contain status information about the placement&nbsp;ID.
