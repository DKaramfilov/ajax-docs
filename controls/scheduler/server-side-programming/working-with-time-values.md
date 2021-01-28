---
title: Working with Time Values
page_title: Working with Time Values - RadScheduler
description: Check our Web Forms article about Working with Time Values.
slug: scheduler/server-side-programming/working-with-time-values
tags: working,with,time,values
published: True
position: 2
---

# Working with Time Values



## 

Because the scheduler stores its time values using UTC, a little extra work is required when working with appointmenttimes programmatically.To help with this extra work, RadScheduler has a pair of methods for converting between the display time (as it appears inthe scheduler)and UTC (as the scheduler stores the date value). These methods are **DisplayToUtc** and**UtcToDisplay**. Each takes a DateTime value as an argument and returns a converted DateTime value.

When adding appointments to the scheduler programmatically, you must converttime values to universal time sothat they willbe displayed properly:





````C#
	
DateTime start = DateTime.Now.ToUniversalTime();
DateTime end = start.AddHours(1);
Appointment apt = new Appointment("1", start, end, "Do it now.");
RadScheduler1.InsertAppointment(apt);  
				
````
````VB.NET
	
Dim start As DateTime = DateTime.Now.ToUniversalTime()
Dim [end] As DateTime = start.AddHours(1)
Dim apt As New Appointment("1", start, [end], "Do it now.")
RadScheduler1.InsertAppointment(apt)  
	
````


# See Also

 * [Handling Time Zones]({%slug scheduler/accessibility-and-internationalization/handling-time-zones%})
