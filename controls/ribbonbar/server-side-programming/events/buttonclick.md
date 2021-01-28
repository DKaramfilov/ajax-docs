---
title: ButtonClick
page_title: ButtonClick - RadRibbonBar
description: Check our Web Forms article about ButtonClick.
slug: ribbonbar/server-side-programming/events/buttonclick
tags: buttonclick
published: True
position: 2
---

# ButtonClick



## 

The server-side **ButtonClick** event occurs when the user clicks on a button, causing a postback.

The event handler function receives two arguments:

1. The **RadRibbonBar** which has fired the event. This argument is of type object, but can be cast to the **RadRibbonBar type**.

1. An EventArgs object with the following properties:

	* **Button** - the clicked button.

	* **Group** - the parent group of the clicked button.

	* **Index** - the index of the clicked button in its containing group.

````ASPNET
<telerik:RadRibbonBar RenderMode="Lightweight" ID="RadRibbonBar1" runat="server" OnButtonClick="RadRibbonBar1_ButtonClick">
    <telerik:RibbonBarTab Text="Home">
        <telerik:RibbonBarGroup Text="Clipboard" EnableLauncher="true">
            <Items>
                <telerik:RibbonBarButton Size="Medium" Text="Cut" ImageUrl="icons/Cut.png" />
                <telerik:RibbonBarButton Size="Medium" Text="Copy" ImageUrl="icons/Copy.png" />
            </Items>
        </telerik:RibbonBarGroup>
    </telerik:RibbonBarTab>
</telerik:RadRibbonBar>
<asp:Literal runat="server" ID="Literal1"></asp:Literal>
````





````C#
	
protected void RadRibbonBar1_ButtonClick(object sender, RibbonBarButtonClickEventArgs e)
{
    Literal1.Text += "Text: " + e.Button.Text + "<br/>";
}
	
````
````VB.NET
		
Protected Sub RadRibbonBar1_ButtonClick(sender As Object, e As RibbonBarButtonClickEventArgs)
    Literal1.Text += "Text: " + e.Button.Text + "<br/>"
End Sub	
	
````


# See Also

 * [Online Demo](https://demos.telerik.com/aspnet-ajax/ribbonbar/examples/events/serverside/defaultcs.aspx)

 * [Server-side Events Overview]({%slug ribbonbar/server-side-programming/events/overview%})
