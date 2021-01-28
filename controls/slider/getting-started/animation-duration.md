---
title: Animation Duration
page_title: Animation Duration - RadSlider
description: Check our Web Forms article about Animation Duration.
slug: slider/getting-started/animation-duration
tags: animation,duration
published: True
position: 4
---

# Animation Duration

**AnimationDuration** defines the length of the slide animation in milliseconds. Setting AnimationDuration to a value larger than 0, will cause the drag slider and selected region to be updated using a linear animationBy default AnimationDuration value is 100 (ms). To disable slide animation set AnimationDuration to 0.

````ASP.NET
<telerik:radslider id="RadSlider1" runat="server" AnimationDuration="500" />
````

````C#
RadSlider1.AnimationDuration = 500;
````
````VB
RadSlider1.AnimationDuration = 500
````

