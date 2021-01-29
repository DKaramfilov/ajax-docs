---
title: End User Restriction
page_title: End User Restriction - RadComboBox
description: Check our Web Forms article about End User Restriction.
slug: combobox/functionality/end-user-restriction
tags: end,user,restriction
published: True
position: 5
---

# End User Restriction



## 

**AllowCustomText** is a property which allows users to type a random text in the RadComboBox's input area. This means that the RadComboBox's input area can contain text that is not encountered as text of an item from the RadComboBox's item collection.

**AllowCustomText** is a boolean property and gets either 'true' or 'false', as a value. When it is set to 'true' - the users are allowed to type text in the input area, when set to 'false' - the input area contains only the currently selected item's text, or text obtained by all selected items' texts separated by comma or other character.

When **AllowCustomText** is **set to 'true'**, the **MaxLength** property controls the number of characters the user can type into the input area.

>caution When **EnableLoadOnDemand** is **enabled** , users are allowed to type in the input area, regardless of the value of **AllowCustomText** .
>


# See Also

 * [Load On Demand Overview]({%slug combobox/load-on-demand/overview%})
