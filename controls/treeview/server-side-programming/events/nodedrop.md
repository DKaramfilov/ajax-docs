---
title: NodeDrop
page_title: NodeDrop - RadTreeView
description: Check our Web Forms article about NodeDrop.
slug: treeview/server-side-programming/events/nodedrop
tags: nodedrop
published: True
position: 4
---

# NodeDrop



## 

When a Node is dropped onto another Node, between other Nodes or onto an HTML element the **NodeDrop** event fires. The **RadTreeNodeDragDropEventArgs** provides properties for the source and destination Nodes:

* **SourceDragNode**: The Node being dropped.

* **DestDragNode**: The Node being dropped onto.

* **DraggedNodes**: A collection of **RadTreeNodes** that are being dragged. This could be useful when **MultipleSelect** is **True**.

* **DropPosition**: Indicates the relationship of the Nodes being dropped and will be a **RadTreeViewDropPosition** enumeration value **Above**, **Below** or **Over**.

* **HtmlElementID**: The **ID** of the HTML element that the Node is being dropped onto.

See [Drag and Drop Overview]({%slug treeview/drag-and-drop/overview%}) for more information.



````C#
protected void RadTreeView1_NodeDrop(object sender, Telerik.Web.UI.RadTreeNodeDragDropEventArgs e)
{
    e.DestDragNode.Nodes.Add(e.SourceDragNode);
} 		
````
````VB.NET
Protected Sub RadTreeView1_NodeDrop(ByVal sender As Object, ByVal e As Telerik.Web.UI.RadTreeNodeDragDropEventArgs)
    e.DestDragNode.Nodes.Add(e.SourceDragNode)
End Sub
````


# See Also

 * [Server-side events Overview]({%slug treeview/server-side-programming/events/overview%})

 * [NodeCheck]({%slug treeview/server-side-programming/events/nodecheck%})

 * [NodeClick]({%slug treeview/server-side-programming/events/nodeclick%})

 * [NodeCollapse]({%slug treeview/server-side-programming/events/nodecollapse%})

 * [NodeCreated]({%slug treeview/server-side-programming/events/nodecreated%})

 * [NodeDataBound]({%slug treeview/server-side-programming/events/nodedatabound%})

 * [NodeEdit]({%slug treeview/server-side-programming/events/nodeedit%})

 * [NodeExpand]({%slug treeview/server-side-programming/events/nodeexpand%})
