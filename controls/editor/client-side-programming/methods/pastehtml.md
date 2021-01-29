---
title: pasteHtml
page_title: pasteHtml - RadEditor
description: Check our Web Forms article about pasteHtml.
slug: editor/client-side-programming/methods/pastehtml
tags: pastehtml
published: True
position: 13
---

# pasteHtml

Pastes HTML content to the cursor position.

|  **function pasteHtml(content)**  |  |  |
| ------ | ------ | ------ |
| **content** | **string** |The HTML content, that will be pasted in Telerik RadEditor|

The following example will show you how to paste content into the editor's content area from an external input button:

````ASP.NET
<telerik:radeditor runat="server" ID="RadEditor1"></telerik:radeditor>
<input type="button" value="Paste Content" onclick="InsertSpan();return false;" />
<script type="text/javascript">
	function InsertSpan()
	{
		var editor = $find("<%=RadEditor1.ClientID%>"); //get a reference to the editor
		editor.pasteHtml('<span style="width:100px;border: 1px solid red;background-color: blue;color: white;">sample content</span>');
	}
</script>   
````

You can find more details on how to get reference to RadEditor in the following article [Getting a Reference to RadEditor](https://docs.telerik.com/devtools/aspnet-ajax/controls/editor/client-side-programming/getting-a-reference-to-radeditor).




