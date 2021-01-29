---
title: Event Handlers Are Not Raised
page_title: Event Handlers Are Not Raised - RadButton
description: Check our Web Forms article about Event Handlers Are Not Raised.
slug: button/troubleshooting/event-handlers-are-not-raised
tags: event,handlers,are,not,raised
published: True
position: 2
---

# Event Handlers Are Not Raised

When RadCompression is enabled and you are using .NET 4.0, event handlers might not be raised in a default document in IIS 7 or IIS 7.5 Integrated Mode, **which could break the normal work of RadButton**.

This problem is caused by a breaking change in .NET 4.0 described in this official [ASP.NET Breaking Changes](https://www.asp.net/learn/whitepapers/aspnet4/breaking-changes#0.1**Toc256770154) section. To workaround it one can set **preCondition="managedHandler"** for the RadCompression module. You may also need to remove the **runAllManagedModulesForAllRequests** setting from your web.config if you have it (or set it to false).

## See Also

 * [RadButton Known Issues in IE6 and IE7]({%slug button/troubleshooting/radbutton-known-issues-in-ie6-and-ie7%})

 * [RadButton Not Performing Postback]({%slug button/troubleshooting/radbutton-not-performing-postback%})

 * [Client-side Click Event Handler Is Not Executed]({%slug button/troubleshooting/client-side-click-event-handler-is-not-executed%})
