---
title: OnClientReminderDismissing 
page_title: OnClientReminderDismissing - RadScheduler
description: Check our Web Forms article about OnClientReminderDismissing.
slug: scheduler/client-side-programming/events/onclientreminderdismissing-
tags: onclientreminderdismissing,
published: True
position: 41
---

# OnClientReminderDismissing 



## 

The OnClientReminderTriggering client-side event handler is called when an appointment reminder has been dismissed by the user,before the command is sent to the server.

Two parameters are passed to the handler:

* **sender**, the scheduler client object;

* **eventArgs**, with three properties:

	* **get_appointment()** - the instance of the appointment.

	* **et_reminder()** - the reminder.

	* **set_cancel()** - used to cancel the event.

This event can be cancelled.
