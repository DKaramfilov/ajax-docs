---
title: OnClientTileDropped
page_title: OnClientTileDropped - RadTileList
description: Check our Web Forms article about OnClientTileDropped.
slug: tilelist/client-side-programming/client-side-events/onclienttiledropped
tags: onclienttiledropped
published: True
position: 6
---

# OnClientTileDropped




The **OnClientTileDropped** event is raised after a [tile]({%slug tilelist/tiles/overview%}) is dropped by the user in the browser. It is *not* cancellable.

The event handler receives two arguments:

1. the [RadTileList object]({%slug tilelist/client-side-programming/tilelist-object%}) that fired the event

1. an event arguments object that exposes the following methods


>caption OnClientTileDropped event arguments object

|  **Name**  |  **Return type**  |  **Description**  |
| ------ | ------ | ------ |
|get_tile()|[RadBaseTile client-side object]({%slug tilelist/tiles/client-side-programming/basetile-object%})|Gets a reference to the tile that is dropped.|

The following example will show how the **OnClientTileDropped** event can be used to **prompt the user to save the changes** that are made to the layout. The full version would require a **RadWindowManager** for the confirmation dialog, a **RadAjaxManager** for the request to the server and a **RadPersistenceManager** to save the state.

````ASP.NET
<telerik:RadTileList RenderMode="Lightweight" EnableDragAndDrop="true" ID="TileList2" runat="server" OnClientTileDropped="OnClientTileDroppedHandler">
	<Groups>
		<telerik:TileGroup>
			<telerik:RadIconTile ImageUrl="Settings.png" runat="server">
			</telerik:RadIconTile>
			<telerik:RadIconTile ImageUrl="Emails.png" runat="server">
			</telerik:RadIconTile>
			<telerik:RadIconTile ImageUrl="Messages.png" runat="server">
			</telerik:RadIconTile>
			<telerik:RadIconTile ImageUrl="Friends.png" runat="server">
			</telerik:RadIconTile>
			<telerik:RadIconTile ImageUrl="Requests.png" runat="server">
			</telerik:RadIconTile>
			<telerik:RadIconTile ImageUrl="Search.png" runat="server">
			</telerik:RadIconTile>
			<telerik:RadIconTile ImageUrl="Account.png" runat="server">
			</telerik:RadIconTile>
		</telerik:TileGroup>
	</Groups>
</telerik:RadTileList>
<telerik:RadWindowManager RenderMode="Lightweight" ID="RadWindowManager1" runat="server">
</telerik:RadWindowManager>
<telerik:RadAjaxManager ID="RadAjaxManager1" runat="server" OnAjaxRequest="OnAjaxRequestHandler">
	<AjaxSettings>
		<telerik:AjaxSetting AjaxControlID="RadAjaxManager1">
			<UpdatedControls>
				<telerik:AjaxUpdatedControl ControlID="TileList2" />
			</UpdatedControls>
		</telerik:AjaxSetting>
	</AjaxSettings>
</telerik:RadAjaxManager>
<telerik:RadPersistenceManager runat="server" ID="RadPersistenceManager1">
<telerik:RadPersistenceManager runat="server" ID="RadPersistenceManager1">
</telerik:RadPersistenceManager>
````



````JavaScript
<telerik:RadCodeBlock runat="server" ID="RadCodeBlock1">
	<script type="text/javascript">
		function OnClientTileDroppedHandler(sender, args) {
			var msg = "You have modified the order of your control panel. Would you like to save the changes?";
			radconfirm(msg, confirmCallBackFn);
		}

		function confirmCallBackFn(arg) {
			if (arg) {
				$find("<%=RadAjaxManager.GetCurrent(Page).ClientID%>").ajaxRequest("storeTileOrder");
			}
		}
	</script>
</telerik:RadCodeBlock>

````





````C#
protected void OnAjaxRequestHandler(object sender, Telerik.Web.UI.AjaxRequestEventArgs e)
{
	if (e.Argument == "storeTileOrder")
	{
		RadPersistenceManager1.SaveState();
	}
}
````
````VB
Protected Sub OnAjaxRequestHandler(sender As Object, e As Telerik.Web.UI.AjaxRequestEventArgs) Handles RadAjaxManager1.AjaxRequest
	If e.Argument = "storeTileOrder" Then
		RadPersistenceManager1.SaveState()
	End If
End Sub
````


