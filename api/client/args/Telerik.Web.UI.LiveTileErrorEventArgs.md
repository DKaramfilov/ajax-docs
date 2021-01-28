---
title: Telerik.Web.UI.LiveTileErrorEventArgs
description: Telerik.Web.UI.LiveTileErrorEventArgs
slug: Telerik.Web.UI.LiveTileErrorEventArgs
---

# Telerik.Web.UI.LiveTileErrorEventArgs : Sys.EventArgs 


Inheritance Hierarchy

* Sys.EventArgs
* [Telerik.Web.UI.LiveTileErrorEventArgs]({%slug Telerik.Web.UI.LiveTileErrorEventArgs%})


## Methods

### get_cancelErrorAlert

Returns a value that indicates whether the error alert will be shown. 

#### Parameters

#### Returns

`Boolean` 

### get_errorMessage

Returns the error message sent from the server. If no such information is available the LiveTile will return "No error data available". 

#### Parameters

#### Returns

`String` 

### set_cancelErrorAlert

Sets a flag that indicates whether the alert with the server error message will be shown to the user. Defaults to false, so an alert will be shown.

#### Parameters

##### value? `Boolean`

#### Returns

`None` 



