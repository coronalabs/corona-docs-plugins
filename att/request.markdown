# att.request()

> --------------------- ------------------------------------------------------------------------------------------
> __Type__				[String][api.type.String]
> __Revision__			[REVISION_LABEL](REVISION_URL)
> __Keywords__			Ads, Monetization, Apple, App Tracking Transparency
> __Platforms__			iOS, tvOS
> --------------------- ------------------------------------------------------------------------------------------


Function, with single listener parameter (to `att` event). This will display the Tracking dialog. Listener will be called with event, which `status` field corresponds to [att.status)][plugin.att.status].

```
local function listener(e)
    eventText.text = "Status is " .. tostring(e.status)
end
att.request(listener)
```
