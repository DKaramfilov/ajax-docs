---
title: Export to JSON
page_title: Export to JSON - RadDiagram
description: Check our Web Forms article about Export to JSON.
slug: diagram/import-and-export/export-to-json
tags: export,to,json
published: True
position: 2
---

# Export to JSON

You can export **RadDiagram** to a JSON object literal on the client. This is done in two simple steps (**Example 1**):

1. Get a reference to the client-side object of the underlying Kendo UI diagram as described in the [Overview]({%slug diagram/client-side-programming/overview%}) help article.

1. Call the [save](https://docs.telerik.com/kendo-ui/api/javascript/dataviz/ui/diagram#methods-save) method of the client-side object of the diagram.

>caption **Example 1**: Export a diagram to a JSON object literal.

````ASP.NET
<telerik:RadDiagram ID="RadDiagra1" runat="server">
	<LayoutSettings Type="Tree" Subtype="Down" Enabled="true">
	</LayoutSettings>
	<ClientEvents OnLoad="onLoad" />
	<ShapesCollection>
		<telerik:DiagramShape Id="DiagramShape1"></telerik:DiagramShape>
		<telerik:DiagramShape Id="DiagramShape2"></telerik:DiagramShape>
	</ShapesCollection>
	<ConnectionsCollection>
		<telerik:DiagramConnection>
			<FromSettings Connector="Top" ShapeId="DiagramShape1" />
			<ToSettings Connector="Bottom" ShapeId="DiagramShape2" />
			<StrokeSettings />
		</telerik:DiagramConnection>
	</ConnectionsCollection>
</telerik:RadDiagram>
<script type="text/javascript">
	function onLoad(diagram) {
		var diagramWidget = diagram.get_kendoWidget();
		var json = diagramWidget.save();
		console.log(json);
	}
</script>
````

You can find a live example of the export to JSON functionality in the [JSON Import and Export demo](https://demos.telerik.com/aspnet-ajax/diagram/examples/saveload/defaultcs.aspx).

# See Also

 * [RadDiagram Client-Side Basics]({%slug diagram/client-side-programming/overview%})

 * [save method of Kendo UI Diagram](https://docs.telerik.com/kendo-ui/api/javascript/dataviz/ui/diagram#methods-save)

 * [RadDiagram JSON Import and Export Demo](https://demos.telerik.com/aspnet-ajax/diagram/examples/saveload/defaultcs.aspx)
