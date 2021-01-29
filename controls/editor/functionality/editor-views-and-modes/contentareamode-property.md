---
title: ContentAreaMode Property
page_title: ContentAreaMode Property - RadEditor
description: Check our Web Forms article about ContentAreaMode Property.
slug: editor/functionality/editor-views-and-modes/contentareamode-property
tags: contentareamode,property
published: True
position: 1
---

# ContentAreaMode Property

**ContentAreaMode** - This property specifies if the content area element of RadEditor is editable IFRAME or DIV. There are two values available for the property: "**Iframe**" and "**Div**". The default value is "Iframe".

These are the main differences between Div and Iframe content area modes:

* When "Iframe" mode is used the content area has a separate document, which does not automatically inherit the current page style sheets. In this mode the parent page CSS styles are copied to the document of the Iframe element by RadEditor. This might decrease the loading performance of the control if multiple styles are defined. In "Div" mode all the styles from the parent page are automatically applied to the content.
 
* When "Div" mode is used, RadEditor will not automatically register stylesheets (e.g., `TableLayoutCssFile`) because they can break the page. If you want to use them, you should add `<link>` elements to the `<head>` of your page manually. When "Iframe" is used, RadEditor adds such stylesheets to the document of the `<iframe>`.

* You cannot edit a [full HTML page](https://demos.telerik.com/aspnet-ajax/editor/examples/completehtmlsupport/defaultcs.aspx)in "Div" mode because the `<html>` element cannot be nested inside a `<div>` element.

* In "Div" mode the content area is part of the current page, which provides better support for https and document.domain cross server scripting.

* The "Div" mode offers better compatibility with some screen readers.

* The "Div" mode supports faster implementation of AutoResizeHeight functionality, which is based on the built-in resize implementation of the DIV element.

* The "Div" content area mode functionality is based on the contentEditable property of the DIV element.All major browsers support this property now, including Firefox 3, Safari 3, Opera 10, Google Chrome, and Internet Explorer (since 5.5), however some older browsers do not.

* One major difference between both modes is that in "Iframe" mode the user can insert FORM tags without breaking the page.

Div mode should be used by experienced users only who know and understand the benefits and the potential problems that may occur.

## See Also

 * [ContentAreaMode='DIV' Property Demo](https://demos.telerik.com/aspnet-ajax/editor/examples/accessibleeditor/defaultcs.aspx)
