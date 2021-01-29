---
title: OnClientGroupPopulated
page_title: OnClientGroupPopulated - RadOrgChart
description: Check our Web Forms article about OnClientGroupPopulated.
slug: orgchart/client-side-programming/events/onclientgrouppopulated
tags: onclientgrouppopulated
published: True
position: 1
---

# OnClientGroupPopulated



## 

If specified, the **OnClientGroupPopulated** client-side event handler is called when the RadOrgChart has received the group items within a node from the Web Service. In the case of server-side binding, the event will not be raised. When client-side binding is used, the event will be raised after the group items are retrieved from the data service. The event will be raised again each time new data has been retrieved from the web service.

Two parameters are passed to the handler:

* **sender** - the RadOrgChart client object;

* **eventArgs** with two properties:

* **get_groupItemCollection() -** retrieves the group items collection within a node.

This event cannot be cancelled.


