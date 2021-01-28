---
title: Telerik.Web.UI.RadToolBarButton
description: Telerik.Web.UI.RadToolBarButton
slug: Telerik.Web.UI.RadToolBarButton
---

# Telerik.Web.UI.RadToolBarButton : Telerik.Web.UI.RadToolBarItem 

## Inheritance Hierarchy

* [Telerik.Web.UI.RadToolBarItem]({%slug Telerik.Web.UI.RadToolBarItem%})
* *[Telerik.Web.UI.RadToolBarButton]({%slug Telerik.Web.UI.RadToolBarButton%})*


## Methods

### blur

Moves focus off the item to the next element in the tab order.

#### Parameters

#### Returns

`None` 

### check

Marks the checkbox of an item.

#### Parameters

#### Returns

`None` 

### click

Causes server-side button click event to occur

#### Parameters

#### Returns

`None` 

### disable

disables the toolbar item.

#### Parameters

#### Returns

`None` 

### enable

Enables the toolbar item.

#### Parameters

#### Returns

`None` 

### focus

Moves focus to the item.

#### Parameters

#### Returns

`None` 

### get_allowSelfUnCheck

Gets a value indicating if a checked button will get unchecked when clicked.

#### Parameters

#### Returns

`Boolean` boolean

### get_animationContainer

Returns the DOM element for the animation container of the item's drop-down list.

#### Parameters

#### Returns

`Element` 

### get_attributes

Returns the collection of custom attributes defined for the item.

#### Parameters

#### Returns

`Object` 

### get_buttons

Returns the collection of items in the drop-down list (if it exists).

#### Parameters

#### Returns

`Telerik.Web.UI.RadToolBarButtonCollection` 

### get_checked

Gets the checked state of an item. The item is checked if get_checked() returns true.

#### Parameters

#### Returns

`Boolean` The value indicating if the item is checked

### get_checkedCssClass

Returns the name of the CSS class applied to the item when checked.

#### Parameters

#### Returns

`String` The value indicating the Css class name

### get_checkedImageUrl

Returns the URL of the image when checked.

#### Parameters

#### Returns

`String` The value indicating the image url

### get_checkOnClick

Marks or unmarks the checkbox of an item when the item is clicked.

#### Parameters

#### Returns

`Boolean` The value indicating if the item is checked

### get_childListElement

Returns the DOM element for the root list of items in the toolbar.

#### Parameters

#### Returns

`Element` DOM element for the root item list

### get_clicked

True if the item is clicked.

#### Parameters

#### Returns

`Boolean` boolean

### get_clickedCssClass

Returns the name of the CSS class applied to the button when clicked.

#### Parameters

#### Returns

`String` The value indicating the Css class name

### get_clickedImageUrl

Returns the URL of the image when it is clicked.

#### Parameters

#### Returns

`String` 

### get_commandArgument

Returns the value of the CommandArgument property.

#### Parameters

#### Returns

`String` string

### get_commandName

Returns the name of the command associated with the item.

#### Parameters

#### Returns

`String` The value indicating the command

### get_defaultButtonIndex

Returns the index of the Default Button.

#### Parameters

#### Returns

`Number` 

### get_disabledCssClass

Gets the CSS class for the item when it is disabled.

#### Parameters

#### Returns

`String` 

### get_disabledImageUrl

Returns the full path to the image of a disabled item

#### Parameters

#### Returns

`String` The value indicating the image url

### get_dropDownElement

Returns the DOM element for the item's drop-down list.

#### Parameters

#### Returns

`Element` 

### get_dropDownVisible

Returns true if the drop-down is opened.

#### Parameters

#### Returns

`Boolean` 

### get_element

Gets the DOM element for the item.

#### Parameters

#### Returns

`Element` 

### get_enabled

true

#### Parameters

#### Returns

`Object` 

### get_enableDefaultButton

Returns true if EnabledDefaultButton is enabled.

#### Parameters

#### Returns

`Object` 

### get_focused

True if the item is focused.

#### Parameters

#### Returns

`Boolean` 

### get_focusedCssClass

Returns the name of the CSS class applied to the button when on focus.

#### Parameters

#### Returns

`String` The value indicating the Css class name

### get_focusedImageUrl

Returns the URL of the image when on focus.

#### Parameters

#### Returns

`String` string

### get_group

Gets the name of the group to which the item belongs.

#### Parameters

#### Returns

`String` The value indicating the name of the group

### get_hovered

True if the item is hovered.

#### Parameters

#### Returns

`Boolean` boolean

### get_hoveredCssClass

Returns the name of the CSS class applied to the button when hovered.

#### Parameters

#### Returns

`String` The value indicating the Css class name

### get_hoveredImageUrl

Returns the URL of the hovered-state image.

#### Parameters

#### Returns

`String` 

### get_imageElement

Gets the image DOM element of the item. If the server side ImageUrl property is not set,  returns null.

#### Parameters

#### Returns

`Element` 

### get_imagePosition

Gets the image position of the toolbar item.

#### Parameters

#### Returns

`Telerik.Web.UI.ToolBarImagePosition` 

### get_imageUrl

Returns the URL of the image.

#### Parameters

#### Returns

`String` 

### get_index

Returns the index of the item in the toolbar or drop-down list.

#### Parameters

#### Returns

`Object` 

### get_innerWrapElement

Gets the DOM element for the innermost SPAN that wraps the item.

#### Parameters

#### Returns

`Element` 

### get_isChecked

True if the item is checked.

#### Parameters

#### Returns

`Boolean` The value indicating if the item is checked

### get_isEnabled

Returns true if both the item and the toolbar are enabled. If one of them is disabled, get_isEnabled() will return false.

#### Parameters

#### Returns

`Object` 

### get_isFirst

Returns whether the item has index 0.

#### Parameters

#### Returns

`Object` 

### get_isLast

Returns whether the item is the last in the toolbar or drop-down list.

#### Parameters

#### Returns

`Object` 

### get_isSeparator

True if the item is separator.

#### Parameters

#### Returns

`Boolean` The value indicating if the item is separator

### get_level

Gets the level of the item. Buttons and child items of a drop down button have 0 level. Child items of a split button are with level 1.

#### Parameters

#### Returns

`Object` 

### get_linkElement

Gets the anchor DOM element of the toolbar item.

#### Parameters

#### Returns

`Element` 

### get_middleWrapElement

Gets the DOM element for the middle SPAN that wraps the item.

#### Parameters

#### Returns

`Element` 

### get_navigateUrl

Returns the URL of the toolbar item(the href attribute of the link). Null if the NavigateUrl server property is not set.

#### Parameters

#### Returns

`String` The value indicating the Url

### get_nextSibling

Returns the next item in the toolbar or drop-down list.

#### Parameters

#### Returns

`Telerik.Web.UI.RadToolBarItem` 

### get_outerWrapElement

Gets the DOM element for the outermost SPAN that wraps the item.

#### Parameters

#### Returns

`Element` 

### get_postBack

True if postback is enabled, false otherwise.

#### Parameters

#### Returns

`Boolean` boolean

### get_postBackUrl

Gets the Url of the page to post to from the current page.

#### Parameters

#### Returns

`String` The value indicating the Url

### get_previousSibling

Returns the previous item in the toolbar or drop-down list.

#### Parameters

#### Returns

`Telerik.Web.UI.RadToolBarItem` 

### get_target

Gets the target of the item. If a target is not set, returns null.

#### Parameters

#### Returns

`String` The value indicating the name of the target

### get_text

Returns the text of the item.

#### Parameters

#### Returns

`String` 

### get_textElement

Gets the DOM element for the text of the item.

#### Parameters

#### Returns

`Element` 

### get_toolBar

Returns the toolbar to which the item belongs.

#### Parameters

#### Returns

`Telerik.Web.UI.RadToolBar` RadToolBar

### get_toolTip

Returns the text of the item's tool tip.

#### Parameters

#### Returns

`String` 

### get_value

Returns the value of the item.

#### Parameters

#### Returns

`Object` 

### get_visible

True if the item is visible.

#### Parameters

#### Returns

`Boolean` boolean

### getDefaultButton

Returns the default button.

#### Parameters

#### Returns

`Telerik.Web.UI.RadToolBarButton` 

### hide

Hides the toolbar item.

#### Parameters

#### Returns

`None` 

### hideDropDown

Closes the drop-down list.

#### Parameters

#### Returns

`None` 

### set_allowSelfUnCheck

Sets a value indicating if a checked button will get unchecked when clicked.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_checked

Marks or unmarks the checkbox of an item.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_checkedCssClass

Sets name of the CSS class applied to the item when checked.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_checkedImageUrl

Sets the name of the CSS class to be applied to the button when checked.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_checkOnClick

Sets marked or unmarked if the item is clicked

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_clickedCssClass

Sets the name of the CSS class to be applied to the button when clicked.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_clickedImageUrl

Sets the URL of the image when it is clicked.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_commandArgument

Sets the value of the CommandArgument property.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_commandName

Sets the name of the command associated with the item.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_defaultButtonIndex

Sets the index of the Default Button.

#### Parameters

##### Int `Number`

#### Returns

`Object` 

### set_disabledCssClass

Sets the CSS class for the item when it is disabled.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_disabledImageUrl

Sets the DisabledImageUrl property of the item

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_enabled

Sets whether the item is enabled.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_enableDefaultButton

Enables/Disables the EnabledDefaultButton mechanism.

#### Parameters

##### boolean `Object`

#### Returns

`Object` 

### set_focused

Sets if the item is focused.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_focusedCssClass

Sets the name of the CSS class to be applied to the button when on focus.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_focusedImageUrl

Sets the URL of the image when on focus.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_group

Sets the name of the group to which the item belongs.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_hoveredCssClass

Sets the name of the CSS class to be applied to the button when hovered.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_hoveredImageUrl

Sets the URL for the hovered-state image.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_imagePosition

Sets the image position of the toolbar item.

#### Parameters

##### value `Telerik.Web.UI.ToolBarImagePosition`

#### Returns

`None` 

### set_imageUrl

Sets the URL for the image.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_isSeparator

Sets if the item is separator.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_navigateUrl

Sets the URL of the item

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_postBack

Determines if the item should postback.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### set_postBackUrl

Sets the Url of the page to post to from the current page.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_target

Sets the target of the Node.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_text

Sets the text of the item.

#### Parameters

##### text `String`

text

#### Returns

`None` 

### set_toolTip

Sets the text of the item's tool tip.

#### Parameters

##### value `String`

value

#### Returns

`None` 

### set_value

Sets the value of the item.

#### Parameters

##### string `Object`

#### Returns

`Object` 

### set_visible

Sets if the item is visible.

#### Parameters

##### value `Boolean`

value

#### Returns

`None` 

### show

Shows the toolbar item.

#### Parameters

#### Returns

`None` 

### showDropDown

Opens the drop-down list.

#### Parameters

#### Returns

`None` 

### toggle

Collapses an expanded toolbar item or expands a collapsed toolbar item.

#### Parameters

#### Returns

`None` 

### unCheck

Unmarks the checkbox of an item.

#### Parameters

#### Returns

`None` 


