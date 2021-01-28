---
title: OnClientTileSelected
page_title: OnClientTileSelected - RadTileList
description: Check our Web Forms article about OnClientTileSelected.
slug: tilelist/client-side-programming/client-side-events/onclienttileselected
tags: onclienttileselected
published: True
position: 9
---

# OnClientTileSelected





The **OnClientTileSelected** event is raised after a [tile]({%slug tilelist/tiles/overview%})is [selected]({%slug tilelist/functionality/selecting%}). It is fired after the [OnClientTileSelecting event]({%slug tilelist/client-side-programming/client-side-events/onclienttileselecting%}), if the latter has not been cancelled. This event is also cancellable.

OnClientTileSelected can be used to cancel the postback (if AutoPostBack is true), but still allows the tile to be selected. Cancelling this event will prevent the postback, but not the selection.

The event handler receives two arguments:

1. the [RadTileList object]({%slug tilelist/client-side-programming/tilelist-object%}) that fired the event

1. an event arguments object that exposes the following methods


>caption OnClientTileSelected event arguments object

|  **Name**  |  **Return type**  |  **Arguments**  |  **Description**  |
| ------ | ------ | ------ | ------ |
|get_cancel()|bool||Gets a value that indicates whether the event is cancelled.|
|get_tile()|[RadBaseTile client-side object]({%slug tilelist/tiles/client-side-programming/basetile-object%})||Gets a reference to the tile that is about to be selected.|
|get_value()|bool||Returns true if the tile is selected.|
|set_cancel(value)||bool|Sets whether the event will be cancelled (if true is passed).|

The following code snippet shows how to get information about a selected tile through the methods exposed by the **OnClientTileSelected** event's arguments. Note that selection is performed by right-clicking on a tile.

````JavaScript
<telerik:RadTileList RenderMode="Lightweight" runat="server" ID="RadTileList1" AutoPostBack="false" OnClientTileSelected="OnClientTileSelected" SelectionMode="Single">
	<Groups>
		<telerik:TileGroup>
			<telerik:RadTextTile Name="Sample Text Tile" Text="Lorem ipsum dolor sit amet" Title-Text="Sample"></telerik:RadTextTile>
		</telerik:TileGroup>
	</Groups>
</telerik:RadTileList>
<div id="myDiv"></div>

<script type="text/javascript">
	function OnClientTileSelected(tileList, args) {
		var tile = args.get_tile();
		var myDiv = document.getElementById("myDiv");
			
		//print tile data
		var log = String.format("Tile with name {0} has been selected; navigateUrl: {1}; selected: {2}; <br />", 
				tile.get_name(), tile.get_navigateUrl(), tile.get_selected());
		myDiv.innerHTML = log;
	}
</script>
````



The example below demonstrates how the **get_value()** method exposed by the **OnClientTileSelected** event arguments can be used to determine whether a tile is selected or deselected.

````JavaScript
<telerik:RadTileList RenderMode="Lightweight" runat="server" ID="RadTileList1" AutoPostBack="true" SelectionMode="Single" OnClientTileSelected="OnClientTileSelected">
	<Groups>
		<telerik:TileGroup>
			<telerik:RadTextTile Name="Sample Text Tile" Text="Lorem ipsum dolor sit amet" Title-Text="Sample" NavigateUrl="https://www.telerik.com"></telerik:RadTextTile>
		</telerik:TileGroup>
	</Groups>
</telerik:RadTileList>

<script type="text/javascript">
	function OnClientTileSelected(tileList, args) {
		var selected = args.get_value();

		if (selected) {
			alert("Tile is now checked.");
			var response = confirm("Do you want to post the page now that the tile is selected?");
			args.set_cancel(!response);//the postback can now be cancelled, not the tile selection
		}
		else {
			alert("Tile is now unchecked.");
		}
	}
</script>
````


