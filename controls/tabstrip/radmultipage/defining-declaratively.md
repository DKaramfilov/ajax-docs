---
title: Defining Declaratively
page_title: Defining Declaratively - RadTabStrip
description: Check our Web Forms article about Defining Declaratively.
slug: tabstrip/radmultipage/defining-declaratively
tags: defining,declaratively
published: True
position: 1
---

# Defining Declaratively

## 

**RadMultiPage** provides a convenient mechanism that lets you define its structure in-line - directly in the .ASPX/.ASCX file.To do this, you need to enclose every **RadPageView** definition in the **&lt;telerik:RadPageView&gt;** ... **&lt;/telerik:RadPageView&gt;** tags:

````ASPNET	  
<telerik:RadMultiPage id="RadMultiPage1" runat="server" SelectedIndex="0" Width="400">
<telerik:RadPageView id="Pageview1" runat="server">
  ...     
</telerik:RadPageView>
<telerik:RadPageView id="Pageview2" runat="server">
  ...       
</telerik:RadPageView>
<telerik:RadPageView id="Pageview3" runat="server">
  ...       
</telerik:RadPageView>
</telerik:RadMultiPage> 	  
````


