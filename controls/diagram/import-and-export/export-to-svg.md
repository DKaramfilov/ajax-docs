---
title: Export to SVG
page_title: Export to SVG - RadDiagram
description: Check our Web Forms article about Export to SVG.
slug: diagram/import-and-export/export-to-svg
tags: export,to,svg
published: True
position: 4
---

# Export to SVG

You can export **RadDiagram** as an SVG document on the client. This is done in two simple steps (**Example 1**):

1. Get a reference to the client-side object of the underlying Kendo UI diagram as described in the [Overview]({%slug diagram/client-side-programming/overview%}) help article.

1. Call the [exportSVG](https://docs.telerik.com/kendo-ui/api/javascript/dataviz/ui/diagram#methods-exportSVG) method of the client-side object of the diagram.

>caution The export to SVG functionality is currently supported in Firefox, Chrome, IE10+ and Opera 15.0+ (Blink).

>caption **Example 1**: Export a diagram as an SVG document.

````ASP.NET
<telerik:RadDiagram ID="RadDiagram1" runat="server">
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
		diagramWidget.exportSVG().done(function (data) {
			kendo.saveAs({
				dataURI: data,
				fileName: "diagram.svg"
			});
		});
	}
</script>
````

You can find a list of the available parameters of the **exportSVG** method in the [Kendo UI Diagram API Reference](https://docs.telerik.com/kendo-ui/api/javascript/dataviz/ui/diagram#methods-exportSVG).

# See Also

 * [RadDiagram Client-Side Basics]({%slug diagram/client-side-programming/overview%})

 * [exportSVG method of Kendo UI Diagram](https://docs.telerik.com/kendo-ui/api/javascript/dataviz/ui/diagram#methods-exportSVG)
