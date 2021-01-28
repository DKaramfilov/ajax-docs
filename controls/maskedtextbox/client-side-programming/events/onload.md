---
title: OnLoad
page_title: OnLoad - RadMaskedTextBox
description: Check our Web Forms article about OnLoad.
slug: radmaskedtextbox/client-side-programming/events/onload
tags: onload
published: True
position: 10
---

# OnLoad



The **OnLoad** client-side event handler is called when the input control is loaded on the client.

Two parameters are passed to the event handler:

* **sender** is the input control.

* **eventArgs** is an instance of [Sys.EventArgs](https://www.asp.net/AJAX/Documentation/Live/ClientReference/Sys/EventArgsClass/default.aspx).

The following example uses the **OnLoad** event to change the background color of a text box:

````ASPNET
<telerik:RadMaskedTextBox RenderMode="Lightweight" ID="RadMaskedTextBox1" runat="server">
	<ClientEvents OnLoad="Load" />
</telerik:RadMaskedTextBox>
````



````JavaScript
<script type="text/javascript">
	function Load(sender)
	{
		sender.get_styles().EnabledStyle[0] += "background-color: lemonchiffon;";
		sender.updateCssClass();
	}
</script>
````


