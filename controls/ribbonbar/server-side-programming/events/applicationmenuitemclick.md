---
title: ApplicationMenuItemClick
page_title: ApplicationMenuItemClick - RadRibbonBar
description: Check our Web Forms article about ApplicationMenuItemClick.
slug: ribbonbar/server-side-programming/events/applicationmenuitemclick
tags: applicationmenuitemclick
published: True
position: 1
---

# ApplicationMenuItemClick



## 

The server-side **ApplicationMenuItemClick** event occurs when the user clicks on application menu item, causing a postback.

The event handler function receives two arguments:

1. The **RadRibbonBar** which has fired the event. This argument is of type object, but can be cast to the **RadRibbonBar type**.

1. An EventArgs object. This object has an **Item** property, which provides access to the item that has just been clicked.

The following example shows how to get the text of the clicked item:



````C#
	
protected void RadRibbonBar1_ApplicationMenuItemClick(object sender, RibbonBarApplicationMenuItemClickEventArgs e)
{
    string message = string.Format("Application menu item {0} was clicked.", e.Item.Text);

    textBox1.Text = message;
}
	
````
````VB.NET
	
Protected Sub RadRibbonBar1_ApplicationMenuItemClick(ByVal sender As Object, ByVal e As RibbonBarApplicationMenuItemClickEventArgs)
	Dim message As String = String.Format("Application menu item {0} was clicked.", e.Item.Text)

	textBox1.Text = message
End Sub
	
````


# See Also

 * [Online Demo](https://demos.telerik.com/aspnet-ajax/ribbonbar/examples/events/serverside/defaultcs.aspx)

 * [Server-side Events Overview]({%slug ribbonbar/server-side-programming/events/overview%})
