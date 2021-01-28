---
title: OnClientCheckCancelled
page_title: OnClientCheckCancelled - RadSpell
description: Check our Web Forms article about OnClientCheckCancelled.
slug: spell/client-side-programming/events/onclientcheckcancelled
tags: onclientcheckcancelled
published: True
position: 2
---

# OnClientCheckCancelled

The **OnClientCheckCancelled** client-side event occurs if the user cancels the spell check. The event handler receives parameters:

1. The spell checker instance that fired the event.

1. Event argument object.

The example below displays a cancellation message in a div.

````ASP.NET
function checkCancelled (sender, args)
{
   $get('statusDiv').innerHTML = 'Spell check was cancelled';
}
...
<div runat="server" id="statusDiv" />        
	   
<telerik:RadSpell
   ID="RadSpell1"
   runat="server"
   ButtonType="PushButton"
   ControlToCheck="TextBox1"
   OnClientCheckCancelled="checkCancelled"
/>  
````


