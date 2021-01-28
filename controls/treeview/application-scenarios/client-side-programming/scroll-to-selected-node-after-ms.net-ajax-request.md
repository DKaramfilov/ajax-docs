---
title: Scroll to Selected Node After MS.NET AJAX Request
page_title: Scroll to Selected Node After MS.NET AJAX Request - RadTreeView
description: Check our Web Forms article about Scroll to Selected Node After MS.NET AJAX Request.
slug: treeview/application-scenarios/client-side-programming/scroll-to-selected-node-after-ms.net-ajax-request
tags: scroll,to,selected,node,after,ms.net,ajax,request
published: True
position: 11
---

# Scroll to Selected Node After MS.NET AJAX Request



## 

To scroll to the selected **TreeNode** after an AJAX request has occurred you should use the **OnEndRequest** client-side event of MS.NET AJAX and select the node in the **OnEndRequest** event handler, like:

````JavaScript	
var prm = Sys.WebForms.PageRequestManager.getInstance();
prm.add_endRequest(OnEndRequest);

function OnEndRequest(sender, args) {
    var tree = $find("<%= RadTreeView1.ClientID %>");
    var selectedNode = tree.get_selectedNode();
	
    if (selectedNode != null) {
        selectedNode.scrollIntoView();
    }
}
````




