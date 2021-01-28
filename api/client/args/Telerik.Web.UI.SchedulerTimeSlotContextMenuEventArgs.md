---
title: Telerik.Web.UI.SchedulerTimeSlotContextMenuEventArgs
description: Telerik.Web.UI.SchedulerTimeSlotContextMenuEventArgs
slug: Telerik.Web.UI.SchedulerTimeSlotContextMenuEventArgs
---

# Telerik.Web.UI.SchedulerTimeSlotContextMenuEventArgs : Sys.EventArgs

## Inheritance Hierarchy

* Sys.EventArgs
* *[Telerik.Web.UI.SchedulerTimeSlotContextMenuEventArgs]({%slug Telerik.Web.UI.SchedulerTimeSlotContextMenuEventArgs%})*


## Methods

### get_domEvent

returns a reference to the DOM event that caused the opening.

#### Parameters

#### Returns

`Sys.UI.DomEvent`
### get_endSlot

Returns the instance of the last time slot in the slot selection.

#### Parameters

#### Returns

`Telerik.Web.UI.ISchedulerTimeSlot`

### get_isAllDay

Returns True if the Time Slot is the 'All Day' slot (Day and Week View only) or False if the Time Slot is a regular one. 

#### Parameters

#### Returns

`Boolean`

### get_startSlot

Returns the instance of the first time slot in the slot selection.

#### Parameters

#### Returns

`Telerik.Web.UI.ISchedulerTimeSlot`

### get_targetSlot

Returns the instance of the time slot on which the user right-clicks.

#### Parameters

#### Returns

`Telerik.Web.UI.ISchedulerTimeSlot`

### get_time

Returns the time on which the user right-clicks in the Time Slot.

#### Parameters

#### Returns

`Date`


