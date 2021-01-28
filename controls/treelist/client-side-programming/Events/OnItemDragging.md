---
title: OnItemDragging
page_title: OnItemDragging - RadTreeList
description: Check our Web Forms article about OnItemDragging Event.
slug: treelist/client-side-programming/Events/OnItemDragging
tags: events,OnItemDragging
published: True
position: 1
---

# OnItemDragging


This event is fired when a TreeListDataItem is being dragged.


| | |
| ------ | ------ |
| **Fired by** | RadTreeList |
| **Arguments** | **get_canDrop()** - bool indicating whether the item can be dropped at that position. This property returns true by default, except if the user is trying to perform an invalid reorder operation - e.g. dropping a parent item over its own child, or dropping an item onto itself. This is useful in the cases, when the developer needs to change the 'drop clue' icon in order to notify the user that it is not possible to perform this operation |
|| **set_canDrop(bool)** - sets a bool indicating whether the item can be dropped at that position. Setting this property to true means that if the user tries to drop the item at this point, all further drag and drop operations will be canceled (OnItemDropping and OnItemDropped events won't be triggered) |
|| **get_domEvent()** - the DOM event |
|| **get_draggedContainer()** - the <tr> element used for representing the dragged row |
|| **get_isOverHeaderItem()** - bool indicating whether the dragged item is over the header item |
|| **get_targetItem()** - gets the target item |
|| **set_dropClueVisible(bool)** - sets whether the drop clue (an arrow image in front of the dragged row) should be visible |
| **Can be canceled** | No |


## Example


````JavaScript
function ItemDragging(sender, eventArgs) {
    console.log("The node is being dragged over the item: " + eventArgs.get_targetItem());
}
````


## See Also

 * [Overview]({%slug treelist/client-side-programming/Events/Overview%})
 
 
 
