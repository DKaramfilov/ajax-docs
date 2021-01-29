---
title: OnClientCommandExecuted
page_title: OnClientCommandExecuted - RadImageEditor
description: Check our Web Forms article about OnClientCommandExecuted.
slug: imageeditor/client-side-programming/events/onclientcommandexecuted
tags: onclientcommandexecuted
published: True
position: 3
---

# OnClientCommandExecuted




The **OnClientCommandExecuted** event is raised after the user fires a command of the control. The event is subsequent to the **OnClientCommandExecuting** event. It cannot be cancelled.

The event handler receives the following parameters:

1. The **RadImageEditor** client instance that fired the event.

1. Event arguments object. You can call its get_commandName() method to get the command name.

````ASP.NET
<telerik:RadImageEditor RenderMode="Lightweight" runat="server" ID="RadImageEditor1" OnClientCommandExecuted="OnClientCommandExecuted"></telerik:RadImageEditor>
<script type="text/javascript">
    function OnClientCommandExecuted(sender, eventArgs)
    {
        alert("OnClientCommandExecuted event fired. Command name was: " + eventArgs.get_commandName());
    }
</script>
````



# See Also

 * [Client-Side Events Basics]({%slug imageeditor/client-side-programming/events/client-side-events-basics%})
