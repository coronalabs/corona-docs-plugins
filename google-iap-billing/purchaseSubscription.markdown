
# store.purchaseSubscription()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [Function][api.type.Function]
> __Return value__      none
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          Google, IAP, in-app purchases, purchase
> __See also__          [store.init()][plugin.google-iap-billing.init]
>						[store.*][plugin.google-iap-billing]
> --------------------- ------------------------------------------------------------------------------------------


## Overview

Initiates a purchase transaction on a provided product by sending out a purchase request to the store, then dispatches a [storeTransaction][plugin.google-iap-billing.event.storeTransaction] event to the listener defined in [store.init()][plugin.google-iap-billing.init].


## Gotchas

This call does not work for subscription purchases.


## Syntax

	store.purchaseSubscription( productIdentifier )

##### productIdentifier ~^(required)^~
_[String][api.type.String]._ String representing the product identifier of the item to purchase.

