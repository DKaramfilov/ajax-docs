---
title: exportToWord
page_title: exportToWord - RadGrid
description: Check our Web Forms article about exportToWord.
slug: grid/client-side-programming/gridtableview-object/methods/exporttoword
tags: exporttoword
published: True
position: 18
---

# exportToWord



## 

Telerik RadGrid can export to MS Word 2003 or later.


|  **exportToWord()**  |
| ------ |
||

Example:

````JavaScript
function ExportGrid() {
    var masterTable = $find("<%=RadGrid1.ClientID %>").get_masterTableView();
    masterTable.exportToWord();

}
````


