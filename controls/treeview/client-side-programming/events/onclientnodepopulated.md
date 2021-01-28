---
title: OnClientNodePopulated
page_title: OnClientNodePopulated - RadTreeView
description: Check our Web Forms article about OnClientNodePopulated.
slug: treeview/client-side-programming/events/onclientnodepopulated
tags: onclientnodepopulated
published: True
position: 5
---

# OnClientNodePopulated



## 

The **OnClientNodePopulated** client-side event occurs when child nodes are loaded on-demand. The **ExpandMode** property of the parent node should be **ServerSideCallback** or **WebService** for this event to fire.

The event handler receives parameters:

1. The **TreeView** instance that fired the event.

1. Event arguments with functions:

* **get_node()** retrieves a reference to the clicked on node.

* **get_domEvent()** retrieves a DOM event object of the node population.

The example below demonstrates retrieving the parent node that is being populated and also getting information about the child nodes.

````ASPNET
<telerik:RadTreeView RenderMode="Lightweight" ID="RadTreeView1" runat="server" OnClientNodePopulated="ClientNodePopulated"
    OnNodeExpand="RadTreeView1_NodeExpand">
    <Nodes>
        <telerik:RadTreeNode runat="server" ExpandMode="ClientSide" Text="Search" ImageUrl="~/images/search.ico"
            Expanded="True" Value="1">
            <Nodes>
                <telerik:RadTreeNode runat="server" ExpandMode="ServerSideCallBack" Text="Recent Searches">
                </telerik:RadTreeNode>
                <telerik:RadTreeNode runat="server" ExpandMode="ServerSideCallBack" Text="Network Locations">
                </telerik:RadTreeNode>
            </Nodes>
        </telerik:RadTreeNode>
    </Nodes>
</telerik:RadTreeView>
````
````JavaScript
function ClientNodePopulated(sender, eventArgs) 
{
	var node = eventArgs.get_node();
	alert("Node " + node.get_text() +
	" is populated with " +
	node.get_nodes().get_count() +
	" child nodes.");
}
````


The server **NodeExpand** event handler for the **RadTreeView** defined above:



````C#
protected void RadTreeView1_NodeExpand(object sender, Telerik.Web.UI.RadTreeNodeEventArgs e)
{
    if (e.Node.Text == "Recent Searches")
    {
        for (int i = 1; i <= 10; i++)
        {
            e.Node.Nodes.Add(new Telerik.Web.UI.RadTreeNode("Search " + i.ToString()));
        }
        e.Node.ExpandMode = Telerik.Web.UI.TreeNodeExpandMode.ClientSide;
    }
    if (e.Node.Text == "Network Locations")
    {
        for (int i = 1; i <= 10; i++)
        {
            e.Node.Nodes.Add(new Telerik.Web.UI.RadTreeNode("Location " + i.ToString()));
        }
        e.Node.ExpandMode = Telerik.Web.UI.TreeNodeExpandMode.ClientSide;
    }
}
````
````VB.NET
Protected Sub RadTreeView1_NodeExpand(ByVal sender As Object, ByVal e As Telerik.Web.UI.RadTreeNodeEventArgs)
    If e.Node.Text = "Recent Searches" Then
        Dim i As Integer = 1
        While i <= 10
            e.Node.Nodes.Add(New Telerik.Web.UI.RadTreeNode("Search " + i.ToString()))
            System.Math.Max(System.Threading.Interlocked.Increment(i), i - 1)
        End While
        e.Node.ExpandMode = Telerik.Web.UI.TreeNodeExpandMode.ClientSide
    End If
    If e.Node.Text = "Network Locations" Then
        Dim i As Integer = 1
        While i <= 10
            e.Node.Nodes.Add(New Telerik.Web.UI.RadTreeNode("Location " + i.ToString()))
            System.Math.Max(System.Threading.Interlocked.Increment(i), i - 1)
        End While
        e.Node.ExpandMode = Telerik.Web.UI.TreeNodeExpandMode.ClientSide
    End If
End Sub
````



# See Also

 * [OnClientNodePopulating]({%slug treeview/client-side-programming/events/onclientnodepopulating%})

 * [RadTreeNode]({%slug treeview/client-side-programming/objects/radtreenode%})

 * [OnClientNodePopulationFailed]({%slug treeview/client-side-programming/events/onclientnodepopulationfailed%})
