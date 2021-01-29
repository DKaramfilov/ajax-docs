---
title: ButtonToggle
page_title: ButtonToggle - RadRibbonBar
description: Check our Web Forms article about ButtonToggle.
slug: ribbonbar/server-side-programming/events/buttontoggle
tags: buttontoggle
published: True
position: 4
---

# ButtonToggle



## 

The server-side **ButtonToggle** event occurs when a toggle button is toggled, causing a postback.

The event handler function receives two arguments:

1. The **RadRibbonBar** which has fired the event. This argument is of type object, but can be cast to the **RadRibbonBar type**.

1. An EventArgs object with the following properties:

	* **Button** - the toggle button that has been toggled.

	* **Group** - the group of the clicked toggle button parent's group.

	* **Index** - the index of the clicked button in its containing group.

The following example shows how to use the properties of the event arguments:



````C#
	
protected void RadRibbonBar1_ButtonToggle(object sender, RibbonBarButtonToggleEventArgs e)
{
    string message = string.Format("ToggleButton {0} was toggled.", e.Button.Text);
    string details = string.Format("Group: {0}, Index: {1}", e.Group.Text, e.Index);

    textBox1.Text = string.Format("{0} {1}", message, details);
}
	
````
````VB.NET
	
Protected Sub RadRibbonBar1_ButtonToggle(ByVal sender As Object, ByVal e As RibbonBarButtonToggleEventArgs)
	Dim message As String = String.Format("ToggleButton {0} was toggled.", e.Button.Text)
	Dim details As String = String.Format("Group: {0}, Index: {1}", e.Group.Text, e.Index)

	textBox1.Text = String.Format("{0} {1}", message, details)
End Sub
	
````


# See Also

 * [Online Demo](https://demos.telerik.com/aspnet-ajax/ribbonbar/examples/events/serverside/defaultcs.aspx)

 * [Server-side Events Overview]({%slug ribbonbar/server-side-programming/events/overview%})
