---
title: Telerik.Web.UI.GridDataBindingEventArgs
description: Telerik.Web.UI.GridDataBindingEventArgs
slug: Telerik.Web.UI.GridDataBindingEventArgs
---

# Telerik.Web.UI.GridDataBindingEventArgs : Sys.CancelEventArgs 

## Inheritance Hierarchy

* Sys.CancelEventArgs
* *[Telerik.Web.UI.GridDataBindingEventArgs]({%slug Telerik.Web.UI.GridDataBindingEventArgs%})*


## Methods

###  get_location

Returns the physical location of the web service/page method which retrieves the data for the grid.

#### Parameters

#### Returns

`String` 

### get_methodArguments

Returns the arguments that will be passed to the method which gets the data (start row index, maximum rows, sort parameter, filter parameter).

#### Parameters

#### Returns

`Object` 

### get_methodName

Returns the name of the method which collects the data.

#### Parameters

#### Returns

`String` 

### set_location

Sets the physical location of the web service/page method which retrieves the data for the grid.

#### Parameters

##### value `String`

#### Returns

`None` 

### set_methodArguments

Sets the arguments that will be passed to the method which gets the data (start row index, maximum rows, sort parameter, filter parameter).

#### Parameters

##### value `Object`

#### Returns

`None` 

### set_methodName

Sets the name of the method which collects the data.

#### Parameters

##### value `String`

#### Returns

`None` 



