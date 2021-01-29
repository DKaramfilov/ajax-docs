---
title: WCAG 2.0 and Section 508 Accessibility Compliance
page_title: WCAG 2.0 and Section 508 Accessibility Compliance - RadNotification
description: Check our Web Forms article about WCAG 2.0 and Section 508 Accessibility Compliance.
slug: notification/accessibility-and-internationalization/wcag-2.0-and-section-508-accessibility-compliance
tags: wcag,2.0,and,section,508,accessibility,compliance
published: True
position: 0
---

# WCAG 2.0 and Section 508 Accessibility Compliance




The interface of **RadNotification for ASP.NET AJAX** is level AA accessible (in compliance with the W3C Web Accessibility Guidelines 2.0) as well as Section 508 compliant. It passes the check of the [WAVE](http://wave.webaim.org/) automated content compliance tool for Section 508 and WCAG 2.0 - Compliance Level AA.

It also offers [WAI-ARIA]({%slug notification/accessibility-and-internationalization/wai-aria-support%}) support.

If automated tools report issues with `<iframe>` elements without a title, they can be considered false positives. They are likely the overlay frames the controls use so they can be shown above heavyweight objects like PDFs or applets. You can disable those frames by setting the `Overlay` and `NotificationMenu.EnableOverlay` properties to `false`.

# See Also

 * [Section 508](http://www.section508.gov/)

 * [Web Content Accessibility Guidelines (WCAG) 2.0](https://www.w3.org/TR/WCAG/)
