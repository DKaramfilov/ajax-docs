---
title: Overview
page_title: Overview - RadChat
description: Check our Web Forms article about Client-side Programming Overview.
slug: chat/client-side-programming/overview
tags: overview
published: True
position: 0
---

# Client-side Programming Overview

The **RadChat** control is a server-side wrapper of the [Kendo UI Chat](https://demos.telerik.com/kendo-ui/chat/index) widget. This allows you to interact with the chat entirely on the client-side.

## Getting the RadChat Client-side Object

**RadChat** creates a client-side object, which can be referred via the **ClientID** of the control and the `$find` function. This allows you to use the API of the RadChat client-side object. The [Get Client-side Reference to a Control Object](https://docs.telerik.com/devtools/aspnet-ajax/general-information/get-client-side-reference) article shows more ways for obtaining a client-side object reference of a control.

Once you obtain a reference to the [RadChat client-side object]({%slug chat/client-side-programming/objects/radchat%}), you can access the underlying Kendo UI Chat widget through the `get_kendoWidget()` method as shown in **Example 1**.

When you have a reference to the Kendo UI Chat widget, you can utilize the [API of the Kendo UI widget](https://docs.telerik.com/kendo-ui/api/javascript/ui/chat). 

>caption  Example 1: Get a reference to the underlying Kendo UI Chat widget.
````JavaScript
var radchat = $find("<%= RadChat1.ClientID %>");
var kendochat = radchat.get_kendoWidget();
````

# See Also

 * [Kendo UI Chat API](https://docs.telerik.com/kendo-ui/api/javascript/ui/chat)

 * [RadChat Client-Side Object]({%slug chat/client-side-programming/objects/radchat%})

 * [Client-Side events Overview]({%slug chat/client-side-programming/events%})

