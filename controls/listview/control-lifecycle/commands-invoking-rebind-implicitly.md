---
title: Commands Invoking Rebind Implicitly
page_title: Commands Invoking Rebind Implicitly - RadListView
description: Check our Web Forms article about Commands Invoking Rebind Implicitly.
slug: listview/control-lifecycle/commands-invoking-rebind-implicitly
tags: commands,invoking,rebind,implicitly
published: True
position: 4
---

# Commands Invoking Rebind Implicitly



## 

This topic lists which internal RadListView commands make an implicit call to the **Rebind**() method of the control in order to refresh its content and fetch the latest information from the data source.

Here is the complete list of commands that trigger **Rebind**():


| Command Name | Field |
| ------ | ------ |
|Update|RadListView.UpdateCommandName|
|Cancel|RadListView.CancelCommandName|
|Delete|RadListView.DeleteCommandName|
|Edit|RadListView.EditCommandName|
|InitInsert|RadListView.InitInsertCommandName|
|PerformInsert|RadListView.PerformInsertCommandName|
|Rebind|RadListView.RebindCommandName|
|Page|RadListView.PageCommandName|
|Sort|RadListView.SortCommandName|
|ChangePageSize|RadListView.ChangePageSize|
|Select|RadListView.SelectCommandName|
|Deselect|RadListView.DeselectCommandName|
