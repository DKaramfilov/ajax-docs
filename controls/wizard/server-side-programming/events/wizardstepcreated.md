---
title: WizardStepCreated
page_title: WizardStepCreated - RadWizard
description: Check our Web Forms article about WizardStepCreated.
slug: wizard/server-side-programming/events/wizardstepcreated
tags: wizardstepcreated
published: True
position: 7
---

# WizardStepCreated



## 

The server-side **OnWizardStepCreated** event occurs when a RadWizardStep object is created.

The **OnWizardStepCreated** event handler receives two arguments:

1. The **RadWizard** that contains the active step. This argument is of type object, but can be cast to the **RadWizard** type.

1. A **WizardStepCreatedEventArgs** object. This object has a property **RadWizardStep** that you can use to access the wizard step that was created.

Use the **OnPreviousButtonClick** event handler to respond when a RadWizardStep object is created.





````C#
protected void RadWizard1_WizardStepCreated(object sender, WizardStepCreatedEventArgs e)
{
	e.RadWizardStep.ToolTip = e.RadWizardStep.Title;
}
````
````VB.NET
Protected Sub RadWizard1_WizardStepCreated(sender As Object, e As WizardStepCreatedEventArgs) Handles RadWizard1.WizardStepCreated
	e.RadWizardStep.ToolTip = e.RadWizardStep.Title
End Sub
````


