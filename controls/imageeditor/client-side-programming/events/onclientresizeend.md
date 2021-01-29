---
title: OnClientResizeEnd
page_title: OnClientResizeEnd - RadImageEditor
description: Check our Web Forms article about OnClientResizeEnd.
slug: imageeditor/client-side-programming/events/onclientresizeend
tags: onclientresizeend
published: True
position: 9
---

# OnClientResizeEnd


 

The **OnClientResizeEnd** event is raised when the user has finished resizing the control.

The event handler receives the following parameters:

1. The **RadImageEditor** client instance that fired the event.

1. Event arguments object.

````ASP.NET
<telerik:RadImageEditor RenderMode="Lightweight" runat="server" ID="RadImageEditor1" OnClientResizeEnd="OnClientResizeEnd"></telerik:RadImageEditor>
<script type="text/javascript">
    function OnClientResizeEnd(sender, eventArgs)
    {
        alert("OnClientResizeEnd event fired by RadImageEditor with ID: " + sender.get_id());
    }
</script>
````



# See Also

 * [Client-Side Events Basics]({%slug imageeditor/client-side-programming/events/client-side-events-basics%})
