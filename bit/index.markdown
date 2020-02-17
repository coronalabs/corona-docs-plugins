# bit.*

> --------------------- ------------------------------------------------------------------------------------------
> __Type__              [library][api.type.library]
> __Revision__          [REVISION_LABEL](REVISION_URL)
> __Keywords__          bit
> __Platforms__			Android, iOS, macOS, Windows
> --------------------- ------------------------------------------------------------------------------------------

## Overview

The Bit plugin provides access to Mike Pall's [Lua BitOp](http://bitop.luajit.org) library.


## Syntax

	local bitLib = require( "plugin.bit" )


## Project Settings

To use this plugin, add an entry into the `plugins` table of `build.settings`. When added, the build server will integrate the plugin during the build phase.

``````lua
settings =
{
	plugins =
	{
		["plugin.bit"] =
		{
			publisherId = "com.coronalabs"
		},
	},
}
``````


## Documentation

[http://bitop.luajit.org/api.html](http://bitop.luajit.org/api.html)


## Support

* [Corona Forums](http://forums.coronalabs.com/forum/631-corona-premium-plugins/)