---
title: Understanding the Skin CSS File
page_title: Understanding the Skin CSS File - RadSlider
description: Check our Web Forms article about Understanding the Skin CSS File.
slug: slider/appearance-and-styling/understanding-the-skin-css-file
tags: understanding,the,skin,css,file
published: True
position: 3
---

# Understanding the Skin CSS File

Styles for **Telerik controls** are defined using Cascading Style Sheet (CSS) syntax. Each style consists of a selector that identifies an HTML element to be styled, and property/value pairs that describe each of the style specifics, e.g. color, padding, margins, etc. See the [CSS Skin File Selectors]({%slug slider/appearance-and-styling/css-classes%}) topic for more information on the specific CSS selectors used for **RadSlider** skins.

Each style maps to a "class" attribute in an HTML tag. For example, consider the HTML rendering of a **RadSlider** control:

## Rendering Horizontal Slider with Items:

The slider control is rendered within a wrapping DIV with **id="RadSliderWrapper_RadSlider_Items"** which specifies the using of RadSlider with Items. For proper rendering two classes were also added: **class=”rslHorizontal rslMiddle”**. The **rslHorizzontal** class defines that the slider will be in horizontal position and the **rslMiddle** class is used when you want to render **Slider with Items** or **Slider with Ticks**. The slider options are rendered with an unordered list. You have four classes for the LI element which are **rslItem** – for each LI element,**rslItemFirst** – only for the first LI element, **rslItemSelected** – only for the selected element and **rslItemLast**- only for the last LI element.

The Handles within the slider are rendered with anchor elements with classes specifying that it is a handle and its functionality – increasing or decreasing the slider: **rslHandle**, **rslDecrease**, **rslIncrease**.

Rendering of the other RadSlider options use the same or very similar HTML semantics. The difference is in the used CSS classes that specify the **Orientation**, **Direction**, **Position**, number of **Drag handles**, **Enabling** or **Disabling** the server-side rendering and **RadSlider** itself. The CSS classes are named sensitively and it is easy to predict what their exact usage is.

![RadSlider with items](images/slider-rs_with_items.gif)

````ASP.NET
<div id="RadSliderWrapper_RadSlider_Items" unselectable="on" style="width: 350px;
	height: 70px;" class="rslHorizontal rslMiddle">
	<a id="RadSliderDecrease_RadSlider_Items" href="#" class="rslHandle rslDecrease"
		title="Decrease"><span>Decrease</span> </a>
	<ul class="rslItemsWrapper">
		<li class="rslItem rslItemFirst rslItemSelected" unselectable="on" style="width: 24px;
			height: 70px;"><span>Jan</span> </li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Feb</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Mar</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Apr</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>May</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Jun</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Jul</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Aug</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Sep</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Oct</span>
		</li>
		<li class="rslItem" unselectable="on" style="width: 24px; height: 70px;"><span>Nov</span>
		</li>
		<li class="rslItem rslItemLast" unselectable="on" style="width: 24px; height: 70px;">
			<span>Dec</span> </li>
	</ul>
	<div unselectable="on" id="RadSliderTrack_RadSlider_Items" class="rslTrack" style="width: 298px;
		height: 6px;">
		<div unselectable="on" id="RadSliderSelected_RadSlider_Items" class="rslSelectedregion"
			style="width: 12px;">
			<!-- -->
		</div>
		<a id="RadSliderDrag_RadSlider_Items" href="#" class="rslDraghandle" title="Drag"
			style="cursor: pointer; left: 8px;"><span>Drag</span> </a>
	</div>
	<a id="RadSliderIncrease_RadSlider_Items" href="#" class="rslHandle rslIncrease"
		title="Increase"><span>Increase</span> </a>
</div>
````



## See Also

 * [Tutorial: Creating a Custom Skin]({%slug slider/appearance-and-styling/tutorial-creating-custom-skin%})

 * [CSS Classes]({%slug slider/appearance-and-styling/css-classes%})
