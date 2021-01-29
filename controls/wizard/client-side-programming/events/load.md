---
title: Load
page_title: Load - RadWizard
description: Check our Web Forms article about Load.
slug: wizard/client-side-programming/events/load
tags: load
published: True
position: 1
---

# Load



The client-side **Load** event is raised when the **RadWizard** client-side object is fully loaded (the full API of the control is available at this point). This article discusses the objects of the control's **Load** event and shows an example of how to retrieve properties when the event occurs (**Example 1**).

To handle this event, simply write a JavaScript function that can be called when the event occurs. Then assign the name of this function as the value of the **OnLoad** property.

## 

The client-side **OnLoad** event handler receives one argument:

* Sender—the [RadWizard object]({%slug wizard/client-side-programming/wizard-object%}) that fired the event.

**Example 1**: Handle the **RadWizard**'s client-side **Load** event.

````ASPNET
<script type="text/javascript">
	function OnClientLoad(sender) {
		var wizard = sender;
		var stepsNumber = wizard.get_wizardSteps().get_count()
		alert("The wizard client-side object is fully loaded and the number of wizard steps are  " + stepsNumber);
	}
</script>

<telerik:RadWizard RenderMode="Lightweight" ID="RadWizard1" runat="server" OnClientLoad="OnClientLoad">
	<WizardSteps>
		<telerik:RadWizardStep Title="Step1">
			<telerik:RadTextBox RenderMode="Lightweight" ID="RadTextBox2" runat="server"></telerik:RadTextBox>
			<telerik:RadTextBox RenderMode="Lightweight" ID="RadTextBox1" runat="server"></telerik:RadTextBox>
		</telerik:RadWizardStep>
		<telerik:RadWizardStep Title="Step2">
			<telerik:RadTextBox RenderMode="Lightweight" ID="RadTextBox3" runat="server"></telerik:RadTextBox>
			<telerik:RadTextBox RenderMode="Lightweight" ID="RadTextBox4" runat="server"></telerik:RadTextBox>
		</telerik:RadWizardStep>
	</WizardSteps>
</telerik:RadWizard>
````


