---
title: OnClientUpdateError
page_title: OnClientUpdateError - RadNotification
description: Check our Web Forms article about OnClientUpdateError.
slug: notification/client-side-programming/events/onclientupdateerror
tags: onclientupdateerror
published: True
position: 6
---

# OnClientUpdateError




The **OnClientUpdateError** event occurs if there has been an error when the **RadNotification** content should be updated. An error alert which can be canceled is displayed.

The event handler receives the following parameters:

1. The **RadNotification** client instance that fired the event.

1. Event arguments object. Call its set_cancelErrorAlert(true) method to cancel the alert.

This code sample will throw the event every time the notification is shown, yet no error alert will be shown to the user and the notification will be empty:

````ASP.NET
<telerik:RadNotification RenderMode="Lightweight" runat="server" ID="RadNotification1" Position="BottomRight"
    Width="250px" Height="100px" OnClientUpdateError="OnClientUpdateError"
    LoadContentOn="EveryShow" ShowInterval="5000" OnCallbackUpdate="OnCallbackUpdate">
</telerik:RadNotification>

<script type="text/javascript">
    function OnClientUpdateError(sender, eventArgs)
    {
        eventArgs.set_cancelErrorAlert(true);
    }
</script>
````





````C#
protected void OnCallbackUpdate(object sender, RadNotificationEventArgs e)
{
    throw (new ApplicationException("an error occured during callback update"));
}
````
````VB
Protected Sub OnCallbackUpdate(sender As Object, e As RadNotificationEventArgs)
    Throw (New ApplicationException("an error occured during callback update"))
End Sub
````



# See Also

 * [Client-Side Events]({%slug notification/client-side-programming/events/overview%})
