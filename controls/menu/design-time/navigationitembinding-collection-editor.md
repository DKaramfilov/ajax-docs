---
title: NavigationItemBinding Collection Editor
page_title: NavigationItemBinding Collection Editor - RadMenu
description: Check our Web Forms article about NavigationItemBinding Collection Editor.
slug: menu/design-time/navigationitembinding-collection-editor
tags: navigationitembinding,collection,editor
published: True
position: 3
---

# NavigationItemBinding Collection Editor

## 

The **NavigationItemBinding Collection Editor** lets you specify how to map the fields from a declarative data source to the properties of the items in your menu. To use the **NavigationItemBinding Collection Builder**, you must first set the **DataSourceID** property. Once the menu is bound to a data source, There are two ways to display the NavigationItemBinding Collection Builder:

* Right-click on the RadMenu control and choose **Edit RadMenu Databindings** from the context menu.

* From the RadMenu [Smart Tag]({%slug menu/design-time/smart-tag%}), choose **Edit RadMenu Databindings...**

![RadMenu NavigationItemBinding Collection Editor </legacyBold>lets you specify how to map the fields from a declarative data source to the properties of the items in your menu. To use the <legacyBold>NavigationItemBinding Collection Builder</legacyBold>, you must first set the <legacyBold>DataSourceID</legacyBold> property. Once the menu is bound to a data source, There are two ways to display the NavigationItemBinding Collection Builde](images/menu_navigationitembindingcollectioneditor.png)

Each item in the collection represents a set of data bindings between the data source and the items in the menu for a given level of the menu (root items, items at the first child level, and so on). You can also create an item that gives the default mapping to cover any levels not specificly mapped by another item.

To add items to the collection, click the **Add** button, and set the item properties in the right hand pane of the dialog.

To delete items from the collection, select the item and click the **Remove** button.

The properties of each item in the collection specify how the **RadMenuItem** properties should be assigned:

* Typically, for each **RadMenuItem** property, there are two properties for the data binding: one is a hard-coded property value that is assigned to all menu items to which the data binding applies, the other is the name of a field from the data source from which the property value can be taken. Thus, for example, the **Text** property and the **TextField** property both set the **Text** of a menu item, but the **Text** property sets the **RadMenuItem** text to a hard-coded string, while the **TextField** property maps it to a field from the data source.

* The **Depth** property indicates the level of menu items to which the data binding applies. If **Depth** is not set, the data binding applies to all menu items not mapped by another binding. The collection should contain only one item with no value assigned to the **Depth** property.

* The **FormatString** property specifies how to format the text supplied by the **TextField** of the data source.

* The **DataMember** property specifies the table from which to map items. This property lets you use different tables from the same **DataSet** to supply values at different levels of the menu.

# See Also

 * [Using DataBindings]({%slug menu/data-binding/using-databindings%})
