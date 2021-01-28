---
title: Forcing a Postback
page_title: Forcing a Postback
description: Check our Web Forms article about Forcing a Postback.
slug: ajaxmanager/client-side-programming/how-to/forcing-a-postback
previous_url: ajax/client-side-programming/how-to/forcing-a-postback
tags: forcing,a,postback
published: True
position: 3
---

# Forcing a Postback



## 

If you want to perform a single postback instead of an AJAX request, **arguments.EnableAjax** should be **false** .

In the code-behind:



````C#
if (!RadAjaxManager1.EnableAJAX)
	{
	     RadAjaxManager1.ClientEvents.OnRequestStart = "OnRequestStart";
	}
	
````
````VB
 If Not RadAjaxManager1.EnableAJAX Then
	    RadAjaxManager1.ClientEvents.OnRequestStart = "OnRequestStart"
End If
````


On the client:

````JavaScript
function OnRequestStart(sender, args) {
	args.set_enableAjax(false); 
}
````



This approach is useful only when you want to perform a single postback. If you want to disable AJAX because of unsupported browsers or old versions of supported ones, we suggest you to do this on the server:



````C#
	
RadAjaxManager1.EnableAJAX = Page.Request.Browser.SupportsXmlHttp;
	
````
````VB
RadAjaxManager1.EnableAJAX = Page.Request.Browser.SupportsXmlHttp
````


## See Also

 * [Cancel AJAX  Request]({%slug ajaxmanager/client-side-programming/how-to/cancel-ajax--request%})

 * [OnRequestStart]({%slug ajaxmanager/client-side-programming/events/onrequeststart%})
