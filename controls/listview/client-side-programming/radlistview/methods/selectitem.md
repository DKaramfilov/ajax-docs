---
title: selectItem
page_title: selectItem - RadListView
description: Check our Web Forms article about selectItem.
slug: listview/client-side-programming/radlistview/methods/selectitem
tags: selectitem
published: True
position: 8
---

# selectItem



## 

Method which selects the **RadListView** item corresponding to the index passed as an argument.


| function selectItem(index) |  |  |
| ------ | ------ | ------ |
| **index** |Integer|The item corresponding to the **index** will be selected.|

````ASP.NET
<telerik:RadCodeBlock ID="RadCodeBlock1" runat="server">
    <script type="text/javascript">
        function SelectFirstItem() {
            var listView = $find("<%= RadListView1.ClientID %>");
            listView.selectItem(0);
        }
    </script>
</telerik:RadCodeBlock>
````


