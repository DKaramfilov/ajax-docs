---
title: Telerik.Web.UI.Editor.CommandBase
description: Telerik.Web.UI.Editor.CommandBase
slug: Telerik.Web.UI.Editor.CommandBase
---

# Telerik.Web.UI.Editor.CommandBase

## Inheritance Hierarchy

* *[Telerik.Web.UI.Editor.CommandBase]({%slug Telerik.Web.UI.Editor.CommandBase%})*


## Methods

### execute

Executes the command.

#### Parameters

#### Returns

`Boolean` Indicates whether the command has been executed successfully or not.

### get_argument

Returns the command arguments. 

#### Parameters

#### Returns

`Object`  

### get_canUnexecute

Indicates whether the command can be executed or not.

#### Parameters

#### Returns

`Boolean`

### get_editor

Returns the RadEditor instance associated to this command.

#### Parameters

#### Returns

`Telerik.Web.UI.RadEditor`

### get_editorContentArea

Returns the value of the RadEditor's ContentAreaMode property.

#### Parameters

#### Returns

`Telerik.Web.UI.EditorContentAreaMode`

### get_enableUndoRedo

Indicates whether the undo/redo functionality is available. 

#### Parameters

#### Returns

`Boolean`

### get_title

Returns the title of the command.

#### Parameters

#### Returns

`String`

### get_window

Returns the window object of the RadEditor's iframe. 

#### Parameters

#### Returns

`Object`

### getState

Returns the command arguments. 

#### Parameters

#### Returns

`Telerik.Web.UI.Editor.CommandStates`  

### getValue

Returns the current value of the command.

#### Parameters

#### Returns

`Object`

### set_canUnexecute

Sets whether the command can be executed or not.

#### Parameters

##### value `Boolean`

#### Returns

`None`

### set_editor

Sets the RadEditor instance associated to this command.

#### Parameters

##### value `Telerik.Web.UI.RadEditor`

#### Returns

`None`

### set_title

Sets the title of the command.

#### Parameters

##### value `String`

#### Returns

`None`

### unexecute

Restores the previous state of the content (i.e., applies undo).

#### Parameters

#### Returns

`None`






