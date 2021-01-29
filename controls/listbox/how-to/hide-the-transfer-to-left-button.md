---
title: Hide the Transfer to Left button
page_title: Hide the Transfer to Left button - RadListBox
description: Check our Web Forms article about Hide the Transfer to Left button.
slug: listbox/how-to/hide-the-transfer-to-left-button
tags: hide,the,transfer,to,left,button
published: True
position: 3
---

# Hide the Transfer to Left button

## 

This article will show how to hide the transfer to left and transfer All to left buttons when the **AllowTransfer=True**.

**SOLUTION**

Add the following CSS rules to the <head> section of your page:

````XML     
<style type="text/css">
	div.RadListBox .rlbTransferTo,
	div.RadListBox .rlbTransferToDisabled,
	div.RadListBox .rlbTransferAllToDisabled,
	div.RadListBox .rlbTransferAllTo
	{
	   display: none;
	}
</style> 		
````

Here is the screenshot of the result - you can transfer items only to the right RadListBox:

![Hide Transfer Left Button](images/listbox_hide_transfer_left_button.png)
