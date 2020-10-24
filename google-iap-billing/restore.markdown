
# store.restore()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google, IAP, in-app purchases, restore
>						[store.purchase()][plugin.google-iap-billing.purchase]
>						[store.*][plugin.google-iap-billing]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Users who wipe the information on a device or buy a new device may wish to restore previously purchased items. This function initiates the process of retrieving all valid purchases and active subscriptions.

During this process, the [storeTransaction][plugin.google-iap-billing.event.storeTransaction] listener defined in [store.init()][plugin.google-iap-billing.init] may be called multiple times, once for each item. Once completed, a transaction state "restoreCompleted" is called.



## Gotchas

Unlike Apple IAP, Google&nbsp;IAP does not include a `"restored"` state for transactions. This function should still be called to retrieve all of the user's purchases, but all valid transactions will be of the `"purchased"` state. When you do a restore, you should treat the returned restored purchases as normal purchases, but avoid making duplicate records in your file or database — essentially, before adding a purchase, check if it already exists in your file/database or overwrite it by its key.


## Syntax

	store.restore()
