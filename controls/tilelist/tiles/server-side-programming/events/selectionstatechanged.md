---
title: SelectionStateChanged
page_title: SelectionStateChanged - RadTile
description: Check our Web Forms article about SelectionStateChanged.
slug: tilelist/tiles/server-side-programming/events/selectionstatechanged
tags: selectionstatechanged
published: True
position: 0
---

# SelectionStateChanged




The **SelectionStateChanged** server-side event is fired when a [Tile is selected]({%slug tilelist/functionality/selecting%}) and **AutoPostBack** is set to **true**. It allows the developer to obtain the selected tile in order to use that information.

The event handler receives two arguments - of type **object** that is a reference to the RadBaseTile control that fired the event and can be cast to it, and a **System.EventArgs** object.

>tip The API of the RadBaseTile object itself is used to obtain the tile selection, so this can be done in any other event. The OnSelectionStateChanged event only provides an immediate event that can be used by the developer.



````ASP.NET
<telerik:RadTextTile ID="Tile1" runat="server" AutoPostBack="true" 
    Text="Tile for selection" 
    OnClick="Tile1_Click">
</telerik:RadTextTile>
<asp:Label Text="" runat="server" ID="Label1"/>
````



Here is an example how to get the selection state of tile:



````C#
protected void Tile1_SelectionStateChanged(object sender, EventArgs e)
{
    Label1.Text = "The Tile is " + (Tile1.Selected ? "selected." : "not selected.");
}
````
````VB
Protected Sub Tile1_SelectionStateChanged(sender As Object, e As EventArgs)
    Label1.Text = "The Tile is " + If(Tile1.Selected, "selected.", "not selected.")
End Sub
````


