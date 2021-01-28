---
title: Right-to-left Support
page_title: Right-to-left Support - RadNotification
description: Check our Web Forms article about Right-to-left Support.
slug: notification/accessibility-and-internationalization/right-to-left-support
tags: right-to-left,support
published: True
position: 1
---

# Right-to-left Support




The **RadNotification** fully supports right-to-left (RTL) language locales. It is created and added to the page root (as a direct child of the form element) and in order to turn on the RTL support you should set **dir=rtl to the html or body** element.

````CSS
html
{
    direction: rtl;
}
````



````ASP.NET
<telerik:RadNotification RenderMode="Lightweight" ID="RadNotification1" runat="server" VisibleOnPageLoad="true"
    ShowTitleMenu="true" Title="Sample Title" Text="Sample notification text" Position="BottomLeft"
    OffsetX="30" OffsetY="-30" Height="100" Width="400" AutoCloseDelay="0" EnableRoundedCorners="true"
    EnableShadow="true">
    <NotificationMenu>
        <Items>
            <telerik:RadMenuItem Text="Sample item 1">
            </telerik:RadMenuItem>
            <telerik:RadMenuItem Text="Sample item 2">
            </telerik:RadMenuItem>
            <telerik:RadMenuItem Text="Sample item 3">
            </telerik:RadMenuItem>
        </Items>
    </NotificationMenu>
</telerik:RadNotification>
````

>caption **Figure 1**:RadNotification in RTL mode

![radnotification-rtl-screenshot](images/radnotification-rtl-screenshot.png)

# See Also

 * [See this live in an online demo](https://demos.telerik.com/aspnet-ajax/notification/examples/righttoleft/defaultcs.aspx)
