---
title: NavigationCommand
page_title: NavigationCommand - RadScheduler
description: Check our Web Forms article about NavigationCommand.
slug: scheduler/server-side-programming/server-events/navigationcommand
tags: navigationcommand
published: True
position: 9
---

# NavigationCommand



The **NavigationCommand** occurs when the user clicks on a control that changes the selected day, view, or mode of the scheduler.

**NavigationCommand** has two parameters:

* **sender** is the scheduler control.

* **e** is an object of type **SchedulerNavigationCommandEventArgs**. It has three properties:

* **Command** indicates what control the user clicked. Possible values are listed in the table below.

* **SelectedDay** is a DateTime specifying the target date when **Command** is **SchedulerNavigationCommand.SwitchToSelectedDay**.

* **Cancel** is a boolean value that lets you prevent the scheduler from responding to the navigation command.

The **Command** property is of type **SchedulerNavigationCommand**. This type has the following possible values:


>caption  

| Name | Description |
| ------ | ------ |
|DisplayNextAppointmentSegment|The user clicked the right-pointing arrow in an appointment to move to the next day.|
|DisplayPreviousAppointmentSegment|The user clicked the left-pointing arrow in an appointment to move to the previous day.|
|NavigateToNextPeriod|The user clicked the right-pointing arrow in the navigation pane.|
|NavigateToPreviousPeriod|The user clicked the left-pointing arrow in the navigation pane.|
|SwitchFullTime|The user clicked the link button in the footer to switch from full-day mode to business hours (or vice versa).|
|SwitchToDayView|The user clicked the Day button of the view tabs when the scheduler was not already in Day view.|
|SwitchToWeekView|The user clicked the Week button of the view tabs when the scheduler was not already in Week view.|
|SwitchToMonthView|The user clicked the Month button of the view tabs when the scheduler was not already in Month view.|
|SwitchToSelectedDay|The user clicked the today button in the navigation pane or the "show more" link in a cell in Month view. The SelectedDay parameter is the day to which the scheduler will be switched.|
|SwitchToMultiDayView|The user clicked the Multi-Day button of the view tabs when the scheduler was not already in Multi-day view.|
|NavigateToSelectedDate|Used when the integrated date picker is the source of the NavigationCommand event.|



## Example

This example disables the "today" button, while still allowing a switch to Day view from a cell in Month view.





````C#
	
protected void RadScheduler1_NavigationCommand(object sender, SchedulerNavigationCommandEventArgs e)
{
	if (e.Command == SchedulerNavigationCommand.SwitchToSelectedDay && RadScheduler1.SelectedView == SchedulerViewType.DayView) 
		e.Cancel = true;
}
	
````
````VB.NET
	
Protected Sub RadScheduler1_NavigationCommand(ByVal sender As Object, _
					 ByVal e As SchedulerNavigationCommandEventArgs) _
							   Handles RadScheduler1.NavigationCommand
	If e.Command = SchedulerNavigationCommand.SwitchToSelectedDay AndAlso _
				  RadScheduler1.SelectedView = SchedulerViewType.DayView Then
		e.Cancel = True
	End If
End Sub
	
	
````


# See Also

 * [NavigationComplete]({%slug scheduler/server-side-programming/server-events/navigationcomplete%})

 * [Views]({%slug scheduler/views/overview%})

 * [Controlling Appearance]({%slug scheduler/appearance-and-styling/controlling-appearance%})

 * [Navigating RadScheduler]({%slug scheduler/usability/navigating-radscheduler%})
