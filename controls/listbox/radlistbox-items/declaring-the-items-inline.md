---
title: Declaring the Items Inline
page_title: Declaring the Items Inline - RadListBox
description: Check our Web Forms article about Declaring the Items Inline.
slug: listbox/radlistbox-items/declaring-the-items-inline
tags: declaring,the,items,inline
published: True
position: 1
---

# Declaring the Items Inline

The definition of **RadListBox** items can be added to the in-line declaration of the ListBox using the **RadListBox Item Builder**. The item builder updates the ASPX or ASCX file to include the list of items and their properties.

You can also directly edit the ASPX or ASCX file by adding items to the <Items></Items> section of the **RadListBox** declaration. Every item definition must be enclosed in \<telerik:RadListBoxItem\> and \</telerik:RadListBoxItem\> tags.

## Example

Add the following **inline** definition of RadListBox to your ASPX or ASCX file:

````ASPNET
<telerik:RadListBox RenderMode="Lightweight" ID="RadListBox2"
   runat="server"
   Skin="Vista">
   <Items>
	   <telerik:RadListBoxItem Text="RadMenu" />
	   <telerik:RadListBoxItem Text="RadComboBox" />
	   <telerik:RadListBoxItem Text="RadListBox" Selected="true" />
   </Items>
</telerik:RadListBox> 
````



At run-time the result will be:

![Inline itemes](images/listbox_inline_items.png)

# See Also

 * [Overview]({%slug listbox/radlistbox-items/overview%})

 * [Loading Items from XML]({%slug listbox/radlistbox-items/loading-items-from-xml%})

 * [Overview]({%slug listbox/data-binding/overview%})

 * [Item Builder]({%slug listbox/design-time/item-builder%})
