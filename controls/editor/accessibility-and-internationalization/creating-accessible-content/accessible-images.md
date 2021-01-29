---
title: Accessible Images
page_title: Accessible Images - RadEditor
description: Check our Web Forms article about Accessible Images.
slug: editor/accessibility-and-internationalization/creating-accessible-content/accessible-images
tags: accessible,images
published: True
position: 3
---

# Accessible Images

An image can be interpreted by the narrative software if you specify an additional description in the "Long Description" field. To make an image accessible fill the **Alt Text** field. For example, insert a pie chart image and fill the box with "Amount Spent Chart". **Long Description** should be set when displaying charts and graphs to provide detailed information. The value of this box should point to a separate description file. For example, create an HTML file named **chartdesc.html** and write more detailed information about the image: *Amount Spent Chart Description. This chart shows the monthly amount spent on different products…*

>caption Figure 1: Specified Long Description field in Image Properties dialog

![Creating Accessible Images](images/editor-creatingaccessibleimages.png)

Here is the produced image tag:

````HTML
<img src="/images/complex_chart.png" alt="Amount Spent Chart" longdesc="chartdesc.html" />	  
````

Information on Alt Attribute [https://www.w3.org/TR/WCAG20-TECHS/H37.html](https://www.w3.org/TR/WCAG20-TECHS/H37.html) Information on LongDesc attribute [https://www.w3.org/TR/WCAG20-TECHS/H45.html](https://www.w3.org/TR/WCAG20-TECHS/H45.html)
