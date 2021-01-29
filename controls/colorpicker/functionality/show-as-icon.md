---
title: Show as Icon
page_title: Show as Icon - RadColorPicker
description: Check our Web Forms article about Show as Icon.
slug: colorpicker/functionality/show-as-icon
tags: show,as,icon
published: True
position: 3
---

# Show as Icon



Use the **ShowIcon** property to display the color picker as an icon. When the user clicks on the icon, the color palette is displayed below the icon. This mode is well suited for scenarios where the color picker is placed on a tool bar.

````ASP.NET
<telerik:RadColorPicker RenderMode="Lightweight" runat="server" ShowIcon="true"/> 
````



When the user clicks the icon, the palette is displayed:

![](images/radcolorpicker013.png)

## ToolTips

Text for the tooltip that appears when the mouse hovers over the icon is controlled by the **PickColorText**and **CurrentColorText**properties.

![](images/radcolorpicker016.png)
