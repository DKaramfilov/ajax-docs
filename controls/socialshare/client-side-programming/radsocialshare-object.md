---
title: RadSocialShare Object
page_title: RadSocialShare Object - RadSocialShare
description: Check our Web Forms article about RadSocialShare Object.
slug: socialshare/client-side-programming/radsocialshare-object
tags: radsocialshare,object
published: True
position: 0
---

# RadSocialShare Object



The **RadSocialShare** client-side object has a number of client-side properties and methods that you can use to manipulate the control in the browser. They are listed below. There are also a number of [client-side events]({%slug socialshare/client-side-programming/events/overview%}) that you can use to produce the logic required by your scenario.

This article contains the following sections:

* [Getters/Setters for the Public Properties](#getterssetters-for-the-public-properties)

* [Methods that Check a Condition or Invoke a Certain Behavior](#methods-that-check-a-condition-or-invoke-a-certain-behavior)

## Getters/Setters for the Public Properties


>caption Getters for the public properties

|  **Name**  |  **Description**  |
| ------ | ------ |
| **get_compactButtons** |Returns the array of compact buttons|
| **get_compactPopup** |Returns the compact popup object (a RadWindow, so its [client-side API]({%slug window/client-side-programming/radwindow-object%}) can be used).|
| **get_emailPopup** |Returns the email popup object (a RadWindow, so its [client-side API]({%slug window/client-side-programming/radwindow-object%}) can be used).|
| **get_fbAppId** |Returns the Facebook Application ID|
| **get_gaEnabled** |Returns value which shows whether Google Analytics is enabled|
| **get_gaID** |Returns the web property ID set for Google Analytics support|
| **get_hideIframesOnDialogMove** |Returns a value which determines whether IFRAMEs are hidden while email or compact popup is being moved|
| **get_mainButtons** |Returns the array of main buttons|
| **get_titleToShare** |Returns the value of the TitleToShare property|
| **get_trackerId** |Returns the Id of the tracker for the RadSocialShare instance|
| **get_urlToShare** |Returns the value of the UrlToShare property|


>caption Setters for the public properties

|  **Name**  |  **Description**  |
| ------ | ------ |
| **set_fbAppId** |Sets the Facebook Application ID|
| **set_gaID** |Sets the web property ID set for Google Analytics support|
| **set_hideIframesOnDialogMove** |Sets a value which determines whether IFRAMEs are hidden while email or compact popup is being moved|
| **set_stringsToShare** |Dynamically sets new values for url and title to share. Takes two strings as arguments - url and title|

## Methods that Check a Condition or Invoke a Certain Behavior


>caption Methods that check a condition or invoke a certain behavior.

|  **Name**  |  **Description**  |
| ------ | ------ |
| **toggleCompactPopup** |Toggles the visibility of the compact popup|
| **toggleEmailPopup** |Toggles the visibility of the email popup|

# See Also

* [RadWindow client-side API]({%slug window/client-side-programming/radwindow-object%})
