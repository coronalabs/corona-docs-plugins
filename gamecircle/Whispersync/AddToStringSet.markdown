# gamecircle.Whispersync.AddToStringSet

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [function][api.type.function]  
> __Library__           [gamecircle.*][plugin.gamecircle]  
> __Return value__      None  
> __Revision__          [REVISION_LABEL](REVISION_URL)  
> __Keywords__          Highest, List, Whispersync  
> --------------------- ------------------------------------------------------------------------------------------


## Overview
Add a value to a string set, which can include [Metadata][plugin.gamecircle.Whispersync.Metadata].

## Syntax
	gamecircle.Whispersync.AddToStringSet(key, value)
	gamecircle.Whispersync.AddToStringSet(key, value, metadata)
	
##### key ~^(required)^~
_[String][api.type.String]._ The key used to access a specific string set.

##### value ~^(require)^~
_[String][api.type.String]._ The value to be added to the string set.

##### metadata ~^(optional)^~
_[Metadata][plugin.gamecircle.Whispersync.Metadata]._ A table of metadata to be stored with the string. It must be a lua table comprised only of string fields with string values in those fields. For examples and more information, check the documentation page for metadata. 

## Examples

``````lua  
local stringSetKey = "myFirstStringSet" 
local gamecircle = require("plugin.gamecircle")   
gamecircle.Init(false, false, true)  
gamecircle.Whispersync.AddToStringSet("A")  
gamecircle.Whispersync.AddToStringSet("B")  
gamecircle.Whispersync.AddToStringSet("C")  
gamecircle.Whispersync.AddToStringSet("D")  
gamecircle.Whispersync.AddToStringSet("E")  
print("Does the set contain F?: " .. gamecircle.Whispersync.StringSetContains(stringSetKey, "F"))  
print("Here is what the string set does contain:")  
local stringSet = gamecircle.Whispersync.GetStringSet(stringSetKey)  
for i,entry in ipairs(stringSet) do  
	print("-" entry.value)  
end  
print("The extra for element A is:")  
local entryA = gamecircle.Whispersync.GetStringSetValue("A")  
print("-value: " .. entryA.value)  
print("-isSet: " .. entryA.isSet)  
print("-metadataPresent: " .. entryA.metadataPresent)  
print("-timestamp: " .. entryA.timestamp)  
local keys = gamecircle.Whispersync.GetHighNumberListKeys()   
for i,key in ipairs(keys) do  
	print("-" .. key)  
end  
``````
