---
title: Getting and Setting Values
page_title: Getting and Setting Values - RadMaskedTextBox
description: Check our Web Forms article about Getting and Setting Values.
slug: radmaskedtextbox/features/getting-and-setting-values
tags: getting,and,setting,values
published: True
position: 3
---

# Getting and Setting Values



On the server-side, each **RadInput** control uses a different property to represent its value. The following table lists the property to use to get or set the value of a **RadInput** control:


| RadInput Control | Property | Type |
| ------ | ------ | ------ |
|RadMaskedTextBox|Text TextWithLiterals TextWithPrompt TextWithPromptAndLiterals|String|
|RadMaskedTextBox|TextWithLiterals TextWithPrompt TextWithPromptAndLiterals|String|
|RadMaskedTextBox|TextWithPrompt TextWithPromptAndLiterals|String|
|RadMaskedTextBox|TextWithPromptAndLiterals|String|


## Common Value Properties

All of the four RadInput controls ( **RadTextBox, RadMaskedTextBox, RadDateInput, and RadNumericTextBox**)have the following common properties:

* The **DisplayText** property allows you to set the display value from the Server to a different value from the actual value. Similar to the empty message, but shown even if the input is not empty. This text will be cleared once the user changes the input value.

* The **ValidationText** is a read-only property which returns the value used to validate the entered data. For the **RadMaskedTextBox** it returns **TextWithLiterals** value( the text the user entered, plus any literal characters in the mask, but no prompt characters. )

The **RadMaskedTextBox** control uses several properties to represent its value, depending on whether you want to include the literal characters from the mask and whether you want to include prompt characters where the user has not yet entered any values. In addition, the property names differ, depending on whether you are using the server-side or client-side object.

On the server side, you can only set the properties that do not include prompt characters. The server-side properties are

* **Text**: the text the user entered into the control. This value does not include any literal characters in the mask or prompt characters.

* **TextWithLiterals**: the text the user entered, plus any literal characters in the mask, but no prompt characters.

* **TextWithPrompt**: the text the user entered, with prompt characters for any characters the user has not yet entered, but with none of the literal characters from the mask. This property is read only.

* **TextWithPromptAndLiterals**: The value as it appears in the control, including the text the user entered plus any prompt characters for characters the user has not yet entered and any literal characters that come from the mask. This property is read only.

On the client side, the properties for the **RadMaskedTextBox** value use the name "**value**" rather than "**Text**".There is no client-side analog to the **TextWithPrompt** property. Only the **value** property (unadorned with prompts or literals) can be set. The client-side properties are

* **get_value**, **set_value**: the text the user entered into the control. This value does not include any literal characters in the mask or prompt characters.

* **get_valueWithLiterals**: the text the user entered, plus any literal characters in the mask, but no prompt characters.

* **get_valueWithPromptAndLiterals**: the value as it appears in the control, including any prompt characters and literal characters from the mask.

The following code examples show how to read the value of one **RadMaskedTextBox** control called "RadMaskedTextBox2" and use it to set the value of another, "RadMaskedTextBox1".


## Server-side



````C#
protected void Page_Load(object sender, EventArgs e)
{
	RadMaskedTextBox1.Text = RadMaskedTextBox2.Text;
}
````
````VB.NET
Protected Sub Page_Load(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Load
	RadMaskedTextBox1.Text = RadMaskedTextBox2.Text
End Sub
````



## Client-side

````JavaScript
function CopyUnMaskedValue()
{
	var radMaskedTextBox1 = $find("<%= RadMaskedTextBox1.ClientID %>");
	var radMaskedTextBox2 = $find("<%= RadMaskedTextBox2.ClientID %>");
	radMaskedTextBox1.set_value(radMaskedTextBox2.get_value());
}

````

