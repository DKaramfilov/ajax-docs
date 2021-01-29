---
title: OnEntryRemoved
page_title: OnEntryRemoved - RadAutoCompleteBox
description: Check our Web Forms article about OnEntryRemoved.
slug: autocompletebox/server-side-programming/events/onentryremoved
tags: onentryremoved
published: True
position: 1
---

# OnEntryRemoved



## 

The **EntryRemoved** event occurs when an entry is removed and InputType="Token" is set for RadAutoCompleteBox.

The **EntryRemoved** event handler receives two arguments:

1. The **RadAutoCompleteBox** object. This argument is of type object, but can be cast to the **RadAutoCompleteBox** type.

1. An AutoCompleteEntryEventArgs object. This object has an **Entry** property of type AutoCompleteBoxEntry.



````C#
	
protected void RadAutoCompleteBox1_EntryRemoved(object sender, AutoCompleteEntryEventArgs e)
{
	Label1.Text = e.Entry.Text + " was removed.";
}
	
````
````VB.NET
	
Protected Sub RadAutoCompleteBox1_EntryRemoved(sender As Object, e As AutoCompleteEntryEventArgs)
	Label1.Text = e.Entry.Text + " was removed."
End Sub
	
````


# See Also

 * [OnEntryAdded]({%slug autocompletebox/server-side-programming/events/onentryadded%})

 * [OnDropDownTemplateNeeded]({%slug autocompletebox/server-side-programming/events/ondropdowntemplateneeded%})

 * [OnTextChanged]({%slug autocompletebox/server-side-programming/events/ontextchanged%})
