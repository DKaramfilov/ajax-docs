---
title: RadSiteMap Item Builder
page_title: RadSiteMap Item Builder - RadSiteMap
description: Check our Web Forms article about RadSiteMap Item Builder.
slug: sitemap/design-time/radsitemap/radsitemap-item-builder
tags: radsitemap,item,builder
published: True
position: 1
---

# RadSiteMap Item Builder



The **RadSiteMap Item Builder** lets you populate your sitemap with a hierarchy of items that do not come from a separate data source. There are two ways to bring up the RadSiteMap Item Builder:

* From the **RadSiteMap** [Smart Tag]({%slug sitemap/design-time/radsitemap/smart-tag%}), click on the **Build RadSiteMap** link.

* Right-click on the **RadSiteMap** component and select **Build RadSiteMap** from its context menu.

## RadSiteMap Item Builder

![RadSiteMap Item Builder](images/sitemap_itembuilder.png)



The **RadSiteMap Item builder** lets you add, rearrange, configure, and delete sitemap items. These actions are initiated using the tool bar at the upper left of the Item builder:

![RadSiteMap iItem Builder Toolbar](images/sitemap_itembuildertoolbar.png)


The following table describes the controls in the tool bar:


| Button | Function |
| ------ | ------ |
|![RadSiteMap Add Item](images/sitemap_additem.png)|Adds a root item to the sitemap in the next available position. Root items are the top-level items (sitemap items with no parent item).|
|![RadSiteMap Add Child Item](images/sitemap_addchilditem.png)|Adds a child item to the currently selected sitemap item. The child can belong to either a root item or another child item.|
|![RadSiteMap Delete Item](images/sitemap_deleteitem.png)|Deletes the currently selected sitemap item. When you delete a sitemap item, its child items are deleted as well.|
|![RadSiteMap Move Level Up](images/sitemap_movelevelup.png)|Moves the currently selected sitemap item up a level, making it a sibling to its parent item (following the parent item).|
|![RadSiteMap Move Level Down](images/sitemap_moveleveldown.png)|Moves the currently selected sitemap item down a level, making it the child of its previous sibling.|
|![RadSiteMap Move Item Up](images/sitemap_moveup.png)|Moves the currently selected sitemap item backward in its current list of siblings, so that it precedes the previous sibling.|
|![RadSiteMap Move Item Down](images/sitemap_movedown.png)|Moves the currently selected sitemap item forward in its current list of siblings, so that it follows the next sibling.|

## 

**RadSiteMap Item Builder**

* **Text** is the text of the item as it appears in the sitemap.

* **ToolTip** is the text of a tooltip that appears when the user hovers the mouse over the item.

* **Enabled** controls whether the item is initially enabled or disabled.

* **Value** lets you associate a text value with the sitemap item that you can use when programming the sitemap behavior.

* **NavigateUrl** and **Target** cause the sitemap item to automatically launch another Web page (specified by **NavigateUrl**) in the window specified by **Target**. If the **Target** property is not set, the new Web page uses the current browser window.

* **CssClass**, **ClickedCssClass**, **DisabledCssClass**, **ExpandedCssClas**, and **FocusedCssClass** control the appearance of the sitemap item when it is in its normal state, clicked, disabled, expanded, and holds input focus, respectively.

* **ImageUrl**, **ImageClickedUrl**, **DisabledImageUrl**, **ExpandedImageUrl**, and **HoveredImageUrl** let you specify an image that appears on the left of the sitemap item when it is in its normal state, clicked, disabled, expanded, and when the mouse hovers over it, respectively.
