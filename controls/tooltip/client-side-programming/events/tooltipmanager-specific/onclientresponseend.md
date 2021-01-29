---
title: OnClientResponseEnd
page_title: OnClientResponseEnd - RadTooltip
description: Check our Web Forms article about OnClientResponseEnd.
slug: tooltip/client-side-programming/events/tooltipmanager-specific/onclientresponseend
tags: onclientresponseend
published: True
position: 2
---

# OnClientResponseEnd





The **OnClientResponseEnd** event is fired immediately after the response from a WebService or an AJAX request is received. This provides an opportunity to make changes just before the content of the tooltip is displayed. It receives two parameters:

1. The RadToolTipManager instance that fired the event. Note that this is not the tooltip that is being shown, this reference should be obtained via the static `getCurrent()` method of the class

1. Event arguments - an empty object that does not expose properties or methods.

````ASP.NET
<script type="text/javascript">
    function OnClientResponseEnd(sender, args)
    {
        var current = Telerik.Web.UI.RadToolTip.getCurrent();
        if (current)
        {
            current.set_modal(false);
        }
    }
</script>
<telerik:RadToolTipManager RenderMode="Lightweight" ID="RadToolTipManager1" OnClientResponseEnd="OnClientResponseEnd">
    <WebServiceSettings Method="GetToolTipData" Path="ToolTipWebService.asmx" />
</telerik:RadToolTipManager>
````


