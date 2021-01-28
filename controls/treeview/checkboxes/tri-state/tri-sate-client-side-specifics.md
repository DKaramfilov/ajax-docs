---
title: Client-side specifics
page_title: Tri-Sate client-side specifics - RadTreeView
description: Check our Web Forms article about Tri-Sate client-side specifics.
slug: treeview/checkboxes/tri-state/tri-sate-client-side-specifics
tags: tri-sate,client-side,specifics
published: True
position: 3
---

# Client-side specifics



## Check State

The **RadTreeNode** client-side object exposes the **get_checkState** function which returns **TreeNodeCheckState** which represents the current state of the Node's checkbox.

**TreeNodeCheckState** can be:

* **0** - Unchecked

* **1** - Checked

* **2** - Indeterminate

## Rendering

The tri-State checkboxes are actually rendered as <*span*> elements with predefined CSS classes. Images, defined in these CSS classes as backgrounds to the <*span*> elements represent the three states.


>caption 

![RadTreeView Tri-State CheckBoxes Rendering](images/treeview_tristatecheckboxesrenderingpng.png)

There are three CSS classes for each of the three states of the checkboxes: **rtChecked**, **rtUnchecked** and **rtIndeterminate**.

To get the <*span*> element of a Node at the client use the **get_checkBoxElement()** function as you would normally do to get the real checkbox element in non tri-state checkboxes mode.

## Events

If a Node's checkbox is clicked the client-side **OnClientNodeClicking** and **OnClientNodeClicked** events fire only for the clicked Node regardless of the **CheckChildNodes** property of **RadTreeView**.


