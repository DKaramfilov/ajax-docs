---
title: OnClientHidden
page_title: OnClientHidden - RadNotification
description: Check our Web Forms article about OnClientHidden.
slug: notification/client-side-programming/events/onclienthidden
tags: onclienthidden
published: True
position: 8
---

# OnClientHidden





The **OnClientHidden** event occurs just after the notification is hidden. The event cannot be cancelled.

The event handler receives the following parameters:

1. The **RadNotification** client instance that fired the event.
1. Event arguments object.

````ASP.NET
<telerik:RadNotification RenderMode="Lightweight" runat="server" ID="RadNotification1" VisibleOnPageLoad="true"
    Position="BottomRight" Width="250px" Height="100px"
    OnClientHidden="OnClientHidden" Text="Sample notification text">
</telerik:RadNotification>

<script type="text/javascript">
    function OnClientHidden(sender, eventArgs)
    {
        alert("OnClientHidden event fired by RadNotification with id: " + sender.get_id());
    }
</script>
````



# See Also

 * [Client-Side Events]({%slug notification/client-side-programming/events/overview%})
