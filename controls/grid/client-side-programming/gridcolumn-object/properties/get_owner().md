---
title: get_owner()
page_title: get_owner() - RadGrid
description: Check our Web Forms article about get_owner().
slug: grid/client-side-programming/gridcolumn-object/properties/get_owner()
tags: get_owner()
published: True
position: 2
---

# get_owner()





## 

Returns a client-side object of type **Telerik.Web.UI.GridTableView** which represents the parent of the current column.

````ASP.NET
<telerik:RadGrid RenderMode="Lightweight" ID="RadGrid1" runat="server" AllowPaging="True"
    OnNeedDataSource="RadGrid1_NeedDataSource">
    <MasterTableView DataKeyNames="OrderID">
    </MasterTableView>
</telerik:RadGrid>
<asp:Button ID="Button9" runat="server" Text="Click"
    OnClientClick="buttonClick(); return false;" />
````



````JavaScript
function buttonClick() {
    var grid = $find('<%= RadGrid1.ClientID %>');
    var masterTableView = grid.get_masterTableView();

    var column = masterTableView.getColumnByUniqueName("ShipCountry");

    // returns a string value representing the column name
    var uniqueName = column.get_uniqueName();

    // corresponding DOM element 
    var columnEl = column.get_element();
    var columnOrder = columnEl.cellIndex;

    // parent table view
    var tableView = column.get_owner();

    // indicates whether the user can reorder this column
    var isReorderable = column.get_reorderable();

    // indicates whether the user can resize this column
    var isResizable = column.get_resizable();

    // indicates whether the user can see this column
    var isVisible = column.get_visible();
}
````


