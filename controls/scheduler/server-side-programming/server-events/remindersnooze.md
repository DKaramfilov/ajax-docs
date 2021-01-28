---
title: ReminderSnooze
page_title: ReminderSnooze - RadScheduler
description: Check our Web Forms article about ReminderSnooze.
slug: scheduler/server-side-programming/server-events/remindersnooze
tags: remindersnooze
published: True
position: 22
---

# ReminderSnooze



## 

The ReminderSnooze event occurs when a reminder has been snoozed.

The event arguments contain:

* **Reminder** - The snoozed reminder with updated Trigger value

* **Appointment** - The original appointment with non-modified reminders

* **SnoozeMinutes** - The snooze minutes value

The operation can be cancelled by setting the **Cancel** property of the event arguments to true.





````C#
	
protected void RadScheduler1_ReminderSnooze(object sender, ReminderSnoozeEventArgs e) 
{ 
	e.Cancel = true; 
}
	
````
````VB
	
Protected Sub RadScheduler1_ReminderSnooze(ByVal sender As Object, ByVal e As ReminderSnoozeEventArgs)
	e.Cancel = True
End Sub
	
````

