---
title: OnClientItemsRequesting
page_title: OnClientItemsRequesting - RadListBox
description: Check our Web Forms article about OnClientItemsRequesting.
slug: listbox/client-side-programming/events/onclientitemsrequesting
tags: onclientitemsrequesting
published: True
position: 14
---

# OnClientItemsRequesting

## 

The **OnClientItemsRequesting** client-side event occurs when **EnableLoadOnDemand** is **True** and the listbox is about to send a server-side request to load more items. This event fires before the items are added to the listbox' Items collection.

The event handler receives two parameters:

1. The instance of the listbox firing the event.

1. An eventArgs parameter containing the following methods:

* **get_context** returns a context object (implements IDictionary) that is passed to the server-side code that handles the request for items.

* **set_cancel** lets you prevent the items request.

This event can be used to cancel the load-on-demand request.

````JavaScript
<script type="text/javascript">
	var shouldCancelEvent = true;
	function OnClientItemsRequesting(sender, eventArgs) {
		eventArgs.set_cancel(shouldCancelEvent);
	}
</script>
````



# See Also

 * [Load On Demand Demo](https://demos.telerik.com/aspnet-ajax/listbox/examples/functionality/loadondemand/defaultcs.aspx)
