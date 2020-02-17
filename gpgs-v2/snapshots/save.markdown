# gpgs.snapshots.save()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [String][api.type.String]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google Play Games Services, game network, gpgs
> __See also__          [gpgs-v2.snapshots.*][plugin.gpgs-v2.snapshots]
>                       [gpgs-v2.*][plugin.gpgs-v2]
> --------------------- ------------------------------------------------------------------------------------------

## Overview

Commits any modifications made to the snapshot. This will cause the changes to be synced to the server in the background.

## Syntax

	gpgs.snapshots.save(params)

##### params ~^(required)^~
_[Table][api.type.Table]._ Contains parameters — see the next section for details.

## Parameter Reference

##### snapshotId ~^(required)^~
_[String][api.type.String]._ Snapshot to save.

##### description ~^(optional)^~
_[String][api.type.String]._ The description of this snapshot to be displayed to the player.

##### playedTime ~^(optional)^~
_[Integer][api.type.Integer]._ The number of milliseconds played by the player.

##### progress ~^(optional)^~
_[Integer][api.type.Integer]._ The progress value.

##### image ~^(optional)^~
_[Table][api.type.Table]._ [Image][plugin.gpgs-v2.type.Image] object. File to upload and use as a snapshot cover image.

##### listener ~^(optional)^~
_[Listener][api.type.Listener]._ Receives [save][plugin.gpgs-v2.snapshots.event.save] event.