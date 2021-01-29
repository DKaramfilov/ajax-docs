---
title: get_contentArea
page_title: get_contentArea - RadEditor
description: Check our Web Forms article about get_contentArea.
slug: editor/client-side-programming/methods/get_contentarea
tags: get_contentarea
published: True
position: 3
---

# get_contentArea

Returns a reference to the editor's content area.

````JavaScript
function get_contentArea()  
````

You can use this method for example to customize the appearance of the editor's content area. The following example demonstrates how to apply different style properties to the content area and change its look:

````ASP.NET
<script type="text/javascript">
	function OnClientLoad(editor, args)
	{
		var style = editor.get_contentArea().style;
		style.backgroundColor = "black";
		style.color = "red";
		style.fontFamily = "Arial";
		style.fontSize = "15";
	}
</script>
<telerik:radeditor runat="server" OnClientLoad="OnClientLoad" ID="RadEditor1"></telerik:radeditor> 
````


