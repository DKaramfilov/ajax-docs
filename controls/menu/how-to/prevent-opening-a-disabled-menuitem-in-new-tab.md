---
title: Prevent Opening a Disabled MenuItem in New Tab
page_title: Prevent Opening a Disabled MenuItem in New Tab - RadMenu
description: Check our Web Forms article about Prevent Opening a Disabled MenuItem in New Tab.
slug: menu/how-to/prevent-opening-a-disabled-menuitem-in-new-tab
tags: prevent,opening,a,disabled,menuitem,in,new,tab
published: True
position: 0
---

# Prevent Opening a Disabled MenuItem in New Tab

## 

This article describes how you can prevent a disabled menu item to open if you right click on it and select Open in new Tab / Window.

Consider the following JavaScript approach to get the desired behavior.

````ASP.NET
<telerik:RadMenuItem runat="server"  
   Text="Disabled"  
   Enabled="false"  
   NavigateUrl="https://www.telerik.com">
</telerik:RadMenuItem> 
````


````JavaScript
//RadMenu for ASP.NET AJAX
var div2 = document.getElementById("RadMenu2");
if (div2.addEventListener) {
    //Firefox way
    div2.addEventListener("contextmenu", onContextMenuAjax, false);
}
else if (div2.attachEvent) {
    //IE way
    div2.attachEvent("oncontextmenu", onContextMenuAjax);
}

function onContextMenuAjax(e) {
    if ($telerik.isIE) {
        //IE way
        if (Sys.UI.DomElement.containsCssClass(e.srcElement.parentElement, 'rmDisabled')) {
            return false;
        }
        else {
            return true;
        }
    }
    else {
        //Firefox way
        if (Sys.UI.DomElement.containsCssClass(e.target.parentNode, 'rmDisabled')) {
            e.stopPropagation();
        }
    }
}
````




