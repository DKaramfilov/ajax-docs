---
title: setSize
page_title: setSize - RadEditor
description: Check our Web Forms article about setSize.
slug: editor/client-side-programming/methods/setsize
tags: setsize
published: True
position: 16
---

# setSize

Sets the width and height of the RadEditor.


|  **function**  **setSize (width, height)**  |  |  |
| ------ | ------ | ------ |
| **width** | **integer** |Sets the width of RadEditor in pixels.|
| **height** | **integer** |Sets the height of RadEditor in pixels.|

>caption Example1: The following example will set the editor's width and height to 600 x 600 pixels when the editor is loaded on the page

````ASP.NET
<script type="text/javascript">
	function OnClientLoad(editor){
		//set the width and height of the RadEditor
		editor.setSize("800","600");
	}
</script>

<telerik:radeditor 
	runat="server" 
	ID="RadEditor1"
	OnClientLoad="OnClientLoad">
</telerik:radeditor>				
````



## See Also

 * [Increase and Decrease Size Buttons]({%slug editor/functionality/toolbars/buttons/examples/increase-and-decrease-size-buttons%})
