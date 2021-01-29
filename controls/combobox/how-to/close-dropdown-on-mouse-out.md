---
title: Close Dropdown on Mouse Out
page_title: Close Dropdown on Mouse Out - RadComboBox
description: Check our Web Forms article about Close Dropdown on Mouse Out.
slug: combobox/how-to/close-dropdown-on-mouse-out
tags: close,dropdown,on,mouse,out
published: True
position: 7
---

# Close Dropdown on Mouse Out



## 

This articles shows how to close the dropdown when the mouse moves out of the dropdown area.

Just add the following javascript code to your aspx page containing the RadComboBox:

````JavaScript
<script type="text/javascript">

$telerik.$(".RadComboBoxDropDown").mouseleave(function () {
	$find("<%= RadComboBox1.ClientID %>").hideDropDown();
});

</script>
````



The javascript code utilizes the [jQuery](http://jquery.com) library which is added in the RadComboBox in the **Q1 2009** release. The above code runs fine in both Internet Explorer and Firefox.

The **mouseleave** event is IE specific and is similar to the mouseout event but with one important difference: the **mouseleave** (and its mouseenter counterpart) **does not bubble**.

The jQuery library successfully converts the mouseleave event to mouseout so it works correctly in Firefox.

# See Also

 * [ASP.NET Ajax Controls and jQuery](https://blogs.telerik.com/atanaskorchev/posts/08-11-06/asp_net_ajax_controls_and_jquery.aspx)
