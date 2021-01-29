---
title: Tracking History
page_title: Tracking History - RadWizard
description: Check our Web Forms article about Tracking History.
slug: wizard/functionality/tracking-history
tags: tracking,history
published: True
position: 2
---

# Tracking History



**Tracking history** is functionality that enables the developer to get the list with the active steps and the order in which they have been activated. This article demonstrates how you can use this functionality on client and server side.

## Tracking history on the client side

In order to track the user interaction with the RadWizard you can use the control client-side **get_history()** method. It returns an array of indexes of the steps that have been activated and they are also arranged in the same order they have been activated.

**Example 1** demonstrates how to add an item to a list that already exists. Each item contains the step title.

````JavaScript
function PrintHistoryButton_ClientClicked(sender, args) {
	var $ = $telerik.$;
	var list = $(".steps");
	var wizard = $find("<%= RadWizard1.ClientID %>");
	var acivatedStepsIndexes = wizard.get_history();
	for (var i = 0; i < acivatedStepsIndexes.length; i++) {
		var currentIndex = acivatedStepsIndexes[i];
		var currentStep = wizard.get_wizardStepByIndex(currentIndex);
		var item = "<li>" + currentStep.get_title() + "</li>";
		$(item).appendTo(list);
	}
}
````



````ASPNET
<telerik:radwizard runat="server" id="RadWizard4" width="800px" height="330px" displaycancelbutton="true">
<WizardSteps>
	<telerik:RadWizardStep ID="RadWizardStep1" Title="Name" StepType="Start">
		<telerik:RadTextBox RenderMode="Lightweight" runat="server" ID="RadTextBox13" Label="First Name" LabelWidth="75px" Width="400px">
		</telerik:RadTextBox>
		<br />
		<telerik:RadTextBox RenderMode="Lightweight" runat="server" ID="RadTextBox14" Label="Middle Name" LabelWidth="75px" Width="400px"></telerik:RadTextBox>
		<br />
		<telerik:RadTextBox RenderMode="Lightweight" runat="server" ID="RadTextBox15" Label="Last Name" LabelWidth="75px" Width="400px"></telerik:RadTextBox>
	</telerik:RadWizardStep>
	<telerik:RadWizardStep ID="RadWizardStep2" Title="Address" DisplayCancelButton="false">
		<telerik:RadTextBox RenderMode="Lightweight" runat="server" ID="RadTextBox16" Label="Country" LabelWidth="75px" Width="400px"></telerik:RadTextBox>
		<br />
		<telerik:RadTextBox RenderMode="Lightweight" runat="server" ID="RadTextBox17" Label="City" LabelWidth="75px" Width="400px"></telerik:RadTextBox>
		<br />
		<telerik:RadTextBox RenderMode="Lightweight" runat="server" ID="RadTextBox18" Label="Address" LabelWidth="75px" Width="400px"></telerik:RadTextBox>
	</telerik:RadWizardStep>
</WizardSteps>
</telerik:radwizard>
<telerik:radbutton runat="server" id="PrintHistoryButton" autopostback="false" onclientclicked="PrintHistoryButton_ClientClicked"></telerik:radbutton>
<p class="hisotryHeader">History of selected steps:</p>
<ul class="steps"></ul>
	
````



>caution The array returned by the **get_history()** method is cleared if a post-back occurs.Therefore this approach will not work if the **RenderedSteps** property is set to **"Active"** or you are subscribed for any **RadWizard** server-side event.
>


## Tracking history on the server side

The RadWizard server-side method **GetHistory** returns the list with the active steps and the order in which they have been activated.

**Example 2** demonstrates how to print the active step titles and the order in which they have been activated on server-side.





````C#
protected void RadWizard1_ActiveStepChanged(object sender, EventArgs e)
{
	History.Text = string.Empty;
	foreach (RadWizardStep step in RadWizard1.GetHistory())
	{
		History.Text += step.Title + ", ";
	}
	History.Text = History.Text.Substring(0, History.Text.Length - 2);
}
````
````VB.NET
Protected Sub RadWizard1_ActiveStepChanged(sender As Object, e As EventArgs)
	History.Text = String.Empty
	For Each [step] As RadWizardStep In RadWizard1.GetHistory()
		History.Text += [step].Title + ", "
	Next
	History.Text = History.Text.Substring(0, History.Text.Length - 2)
End Sub
````

# See Also

 * [Wizard - Tracking History](https://demos.telerik.com/aspnet-ajax/wizard/functionality/tracking-history/defaultcs.aspx)

