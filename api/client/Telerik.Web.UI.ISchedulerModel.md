---
title: Telerik.Web.UI.ISchedulerModel
description: Telerik.Web.UI.ISchedulerModel
slug: Telerik.Web.UI.ISchedulerModel
---

# Telerik.Web.UI.ISchedulerModel  

## Inheritance Hierarchy

* *[Telerik.Web.UI.ISchedulerModel]({%slug Telerik.Web.UI.ISchedulerModel%})*


## Methods

###  getTimeSlotForAppointment

Gets the time slot that will contain the specified appointment if it's added to the scheduler.

#### Parameters

##### appointment `Telerik.Web.UI.SchedulerAppointment`

 The appointment for which to find the time slot. 

#### Returns

`Telerik.Web.UI.ISchedulerTimeSlot`  The time slot instance associated with the specified DOM element. 

### get_visibleRangeEnd

Gets the last visible date of the current view.

#### Parameters

#### Returns

`Date`  The last visible date of the current view. 

### get_visibleRangeStart

Gets the first visible date of the current view.

#### Parameters

#### Returns

`Date`  The first visible date of the current view. 


### getTimeSlotFromDomElement

Gets the time slot associated with the specified DOM element.

#### Parameters

##### domElement `Element`

 The time slot DOM element 

#### Returns

`Telerik.Web.UI.ISchedulerTimeSlot`  The time slot instance associated with the specified DOM element. 


