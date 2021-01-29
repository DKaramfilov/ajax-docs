---
title: Pass More than one Argument
page_title: Pass More than one Argument
description: Check our Web Forms article about Pass More than one Argument.
slug: ajaxpanel/client-side-programming/how-to/pass-more-than-one-argument
tags: pass,more,than,one,argument
published: True
position: 2
---

# Pass More than one Argument



## 

By default, the **ajaxRequest** and **ajaxRequestWithTarget** functions accept only one argument. Sometimes you might need to pass more arguments. You can do this by joining the arguments on the client:

````JavaScript
var arg3 = arg1 + "," + arg2;
ajaxPanel.ajaxRequest(arg3);
````


and split them on the server in the **RadAjaxPanel1_AjaxRequest** :



````C#
private void RadAjaxPanel1_AjaxRequest(object sender, AjaxRequestEventArgs e)
{
	string argument = (e.Argument);
	String[] stringArray = argument.Split(",".ToCharArray());
}			
````
````VB.NET
Protected Sub RadAjaxPanel1_AjaxRequest(ByVal sender As Object, ByVal e As AjaxRequestEventArgs) Handles RadAjaxPanel1.AjaxRequest
	Dim argument As String = e.Argument
	Dim stringArray As [String]() = argument.Split(",".ToCharArray())
End Sub
	
	
````


## See Also

 * [Overview]({%slug ajaxpanel/client-side-programming/overview%})

 * [OnAjaxRequest]({%slug ajaxpanel/server-side-programming/events/onajaxrequest%})
