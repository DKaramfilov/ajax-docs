---
title: Change the End Date When the Start Date Changes
page_title: Change the End Date When the Start Date Changes - RadScheduler
description: Check our Web Forms article about Change the End Date When the Start Date Changes.
slug: scheduler/how-to/change-the-end-date-when-the-start-date-changes
tags: change,the,end,date,when,the,start,date,changes
published: True
position: 8
---

# Change the End Date When the Start Date Changes



This article will show how to change the End Date when the Start Date has changed in the advanced insert or edit form. The End Date will be equal to the new value of the Start Date.

Here are the steps:

1. Subscribe to the [OnFormCreated]({%slug scheduler/server-side-programming/server-events/formcreated%}) event and find the **RadDatePicker** object.Then subscribe to its **OnDateSelected** event:

	**C#**
	     
		protected void RadScheduler1_FormCreated(object sender, SchedulerFormCreatedEventArgs e)
		{    
			RadDatePicker startDate = e.Container.FindControl("StartDate") as RadDatePicker;    
			if (startDate != null)    
			{        
				// advanced form is shown        
				startDate.ClientEvents.OnDateSelected = "changeEndDate";    
			}
		}
				

	**VB**
	
		Protected Sub RadScheduler1_FormCreated(ByVal sender As Object, ByVal e As SchedulerFormCreatedEventArgs)
			Dim startDate As RadDatePicker = TryCast(e.Container.FindControl("StartDate"), RadDatePicker)
			If startDate IsNot Nothing Then
				' advanced form is shown  
				startDate.ClientEvents.OnDateSelected = "changeEndDate"
			End If
		End Sub
	
2. Define the changeEndDate javascript method as follows:

	**JavaScript**
	     
		<telerik:RadScriptBlock ID="RadScriptBlock1" runat="server">
		function changeEndDate(sender, e)
		{    
			var endDatePickerID = sender.get_id().replace("StartDate", "EndDate");    
			var endDatePicker = $find(endDatePickerID);    
			endDatePicker.set_selectedDate(sender.get_selectedDate());
		}
		</telerik:RadScriptBlock>
				

