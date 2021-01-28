---
title: OnClientItemsRequested
page_title: OnClientItemsRequested - RadListBox
description: Check our Web Forms article about OnClientItemsRequested.
slug: listbox/client-side-programming/events/onclientitemsrequested
tags: onclientitemsrequested
published: True
position: 15
---

# OnClientItemsRequested

## 

The **OnClientItemsRequested** client-side event occurs after the load-on-demand mechanism has added new items to the listbox.

The event handler receives the following parameter:

1. The instance of the listbox firing the event.

````JavaScript
<script type="text/javascript">
	function OnClientItemsRequested(sender, eventArgs) {
		alert("There are " + sender.get_items().get_count() + " items.");
	}
</script>
````

# See Also

 * [Load On Demand Demo](https://demos.telerik.com/aspnet-ajax/listbox/examples/functionality/loadondemand/defaultcs.aspx)
