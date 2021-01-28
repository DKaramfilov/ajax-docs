---
title: OnClientInit
page_title: OnClientInit - RadEditor
description: Check our Web Forms article about OnClientInit.
slug: editor/client-side-programming/events/onclientinit
tags: onclientinit
published: True
position: 1
---

# OnClientInit

This event is fired before the initialization of the editor's content area. You can use this method to override the editor's methods, filters, etc. This event prior to the [OnClientLoad]({%slug editor/client-side-programming/events/onclientload%}) event.

|  **function OnClientInit(editor, args)**  |  |  |
| ------ | ------ | ------ |
| **editor** | **object** |Returns a reference to RadEditor client object|
| **args** | **object** |Returns the needed information about the event|

The example below demonstrates how to fix the RadEditor width in case the Editor is added dynamically to the page and its CSS files have not yet been able to load when it is shown, which results in the Editor having bigger width than the expected.

````ASP.NET
<script type="text/javascript">
	function OnClientInit(editor)
	{
		var editorWidth = editor.get_element().style.width;

		editor.add_firstShow(function ()
		{
			editor.get_element().style.width = editorWidth;
		});
	} 
</script> 
<telerik:radeditor runat="server" ID="RadEditor1" OnClientInit="OnClientInit"></telerik:radeditor>
````


