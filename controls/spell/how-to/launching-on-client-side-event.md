---
title: Launching on Client-side Event
page_title: Launching on Client-side Event - RadSpell
description: Check our Web Forms article about Launching on Client-side Event.
slug: spell/how-to/launching-on-client-side-event
tags: launching,on,client-side,event
published: True
position: 1
---

# Launching on Client-side Event

## Scenario

How to launch the spellchecker on various client-side events.

## Solution

The spellchecker is started with a JavaScript function call on the client and can be invoked from a client-side event handler. For example, a TextBox control can be set to automatically check the spelling of its text once the user is finished typing and moves on to another control. This approach can be used to bind the spellchecker to any client-side event.

Follow the steps below to achieve this scenario:

1. We will assume that the TextBox control you want to check has ID of "TextBox1".

1. Set the **RadSpell ButtonType** property to **None**. This will hide the default spellcheck button from the form:

	**ASP.NET**

		<telerik:radspell id="RadSpell1" runat="server" controltocheck="TextBox1" buttontype="None" /> 			

1. Add a JavaScript function to the web page that starts the spellchecker. In this example the function is called "spellCheck()".

	**JavaScript**

		function spellCheck() {
			var spell = $find('<%= RadSpell1.ClientID %>');
			spell.startSpellCheck();
		}	

1. Make the TextBox control **onBlur** client-side handler call the new spellCheck() function:

	**ASP.NET**
	
		<asp:TextBox id="TextBox1" onblur="javascript: spellCheck();" runat="server">this is a mistakr</asp:TextBox> 			

		
