---
title: Right-to-left Support
page_title: Right-to-left Support - RadSpell
description: Check our Web Forms article about Right-to-left Support.
slug: spell/accessibility-and-internationalization/right-to-left-support
tags: right-to-left,support
published: True
position: 2
---

# Right-to-left Support

The **RadSpell** fully supports right-to-left (RTL) language locales. In order to turn on the RTL support you should set its **DialogsCssFile** property to an external CSS file in which you have the **direction: rtl** property set for the html or body element.

>caption dialogsRTL.css
````CSS
body
{
	direction: rtl;
}
````

````ASP.NET
<div dir="rtl">
	 <asp:TextBox ID="TextBox1" runat="server" Height="100" TextMode="MultiLine">mizpelled conttent</asp:TextBox><br />
	 <telerik:RadSpell RenderMode="Lightweight" ID="RadSpell1" runat="server" ControlToCheck="TextBox1" DialogsCssFile="dialogsRTL.css" />
</div>
````

![radspell-rtl-screenshot](images/radspell-rtl-screenshot.png)

# See Also

 * [See this live in an online demo](https://demos.telerik.com/aspnet-ajax/spell/examples/righttoleft/defaultcs.aspx)
