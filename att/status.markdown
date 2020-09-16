# att.status

> --------------------- ------------------------------------------------------------------------------------------
> __Type__				[String][api.type.String]
> __Revision__			[REVISION_LABEL](REVISION_URL)
> __Keywords__			Ads, Monetization, Apple, App Tracking Transparency
> __Platforms__			iOS, tvOS
> --------------------- ------------------------------------------------------------------------------------------

Returns current tracking status. Possible values are:

- `authorized`
- `denied`
- `restricted`
- `notDetermined`
- `unavailable`

```
print(att.status)
```