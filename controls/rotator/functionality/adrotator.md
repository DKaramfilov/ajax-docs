---
title: AdRotator
page_title: AdRotator - RadRotator
description: Check our Web Forms article about AdRotator.
slug: rotator/functionality/adrotator
tags: adrotator
published: True
position: 1
---

# AdRotator

## AdRotator functionality

RadRotator can be easily configured to animate through a set of images that reside into a single directory. All that needs to be done is setting the **BannersPath** property to the virtual path of the images’ directory and the control will be ready for use (of course assuming that the Rotator’s and its items’ dimensions are set, which is required for all RotatorTypes). The control will handle the creation of the items and the item’s html template. This functionality can be used with all RotatorTypes, giving you the ability to choose the right type for your specific scenario. Below you will find the basic facts about the feature and how to use it, as well as tutorial to get you started.

### When to Use

Basically, when you have a folder of images and you want the Rotator to play them, you should use the BannersPath property. If you need more customized solution, then you should consider making your own data source and ItemTemplate, and bind the control to this data source.

### BannersPath property

The default value of the **BannersPath** property is **string.Empty**. Setting this property to non-empty string will cause the Rotator to search for images in the specified directory. Virtual path should be provided, and it is recommended that it starts with ‘~’ (tilde) so it is relative to the applications root directory. It doesn’t matter if the path ends with path separator (i.e. ‘/’) or not. The Rotator will work its way, as long as the directory exists. This means that **“~/Images”** is as good as **“~/Images/”**.	The property can be set in the .aspx markup, as well as in the code-behind. Page.Load or events of postback controls (Button.Click, DropDownList.SelectedIndexChanged) are good place for setting this property.

### Supported Image Formats

The following image formats are supported: *.jpg, .jpeg, .gif, .png, .bmp*. If you want to include different image types, then the **Telerik.Web.UI.RadRotator** class should be inherited and the protected **GetImageExtensions()** overridden. Then you should return a different string of comma separated extensions, keeping in mind that the string should end with comma. This is example that includes only GIF and PNG images:

````C#
protected override string GetImageExtensions()
{
	return "*.gif,*.png,";
}
````
````VB
Protected Overrides Function GetImageExtensions() As String
	Return "*.gif,*.png,"
End Function
````

### Accessing the Items in the Code-Behind

The Rotator requests for the images **OnPreRender**, which means that if you want to access the **RadRotator.Items** collection earlier in the page life-cycle you need to force the Rotator to request its items. This is done by calling the **RadRotator.BindToBanners(forceBind)** method. Note that the forceBind parameter is optional, and by default its value is **false**. In case your scenario requires that the rotator should explicitly request for its items from the server, then pass **true** to this method.

### Modifying the Items

In some scenarios you might want to have direct control on which images are selected and added to the Rotator. There are two options of handling this:

1. Handling the RadRotator.**ItemDataBound** and modifying the items according to your specific logic.

1. Inheriting the Telerik.Web.UI.**RadRotator** class and overriding the **GetBanners(string virtualPath, string allowedExtensions)** method, which should return a collection of type List<Telerik.Web.UI.Rotator.**BannerDataItem**>.The following steps will help you achieve this:

	1. In your project create a new class that inherits the **RadRotator** class.

	1. Override the **GetBanners** method in order to implement your logic for retrieving the rotator images. For example the method from **Example 1** will look for images not only in the currently specified directory, but also all the images in the subdirectories:

	1. Register the class you added on the page that you will use the custom RadRotator:

		**ASP.NET**

			<%@ Register Namespace="CustomWebControls" TagPrefix="webControls" %>

	1. Add an instance of the custom control:

		**ASP.NET**
		
			<webControls:CustomRotator runat="server" ID="RadRotator1" Width="320px" ItemWidth="160px"
				Height="120px" ItemHeight="113px" BannersPath="~/Images">
			</webControls:CustomRotator>
		
>caption **Example 1**: Override the RadRotator's GetBanners method.

````C#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using Telerik.Web.UI;
using Telerik.Web.UI.Rotator;
using System.IO;

namespace CustomWebControls
{
	public class CustomRotator : RadRotator
	{
		protected override List<BannerDataItem> GetBanners(string virtualPath, string allowedExtensions)
		{
			//Get the directory with the images
			var physicalPath = MapPathSecure(virtualPath);
			DirectoryInfo dir = new DirectoryInfo(physicalPath);
			if (!dir.Exists)
			{
				return null;
			}

			var ads = new List<BannerDataItem>();
			var extensionsArray = allowedExtensions.Split(',');

			var physicalPathLength = physicalPath.Length;

			//Loop through the extensions and create the List of images
			foreach (var extension in extensionsArray)
			{
				if (string.IsNullOrEmpty(extension))
					continue;

				FileInfo[] files = dir.GetFiles(extension, SearchOption.AllDirectories);
				foreach (var file in files)
				{
					var fName = file.FullName.Substring(physicalPathLength).Replace("\\", "/");
					ads.Add(new BannerDataItem()
					{
						ImageUrl = string.Concat(virtualPath, fName),
						AlternateText = file.Name,
					});
				}
			}

			return ads;
		}
	}
}
````
````VB
Imports Microsoft.VisualBasic
Imports System.Collections.Generic
Imports System.Linq
Imports System.Web
Imports Telerik.Web.UI
Imports Telerik.Web.UI.Rotator
Imports System.IO

Namespace CustomWebControls
	Public Class CustomRotator
		Inherits RadRotator
		Protected Overrides Function GetBanners(virtualPath As String, allowedExtensions As String) As List(Of Telerik.Web.UI.Rotator.BannerDataItem)
			'Get the directory with the images
			Dim physicalPath = MapPathSecure(virtualPath)
			Dim dir As New DirectoryInfo(physicalPath)
			If Not dir.Exists Then
				Return Nothing
			End If

			Dim ads = New List(Of BannerDataItem)()
			Dim extensionsArray = allowedExtensions.Split(","c)

			Dim physicalPathLength = physicalPath.Length

			'Loop through the extensions and create the List of images
			For Each extension As String In extensionsArray
				If String.IsNullOrEmpty(extension) Then
					Continue For
				End If

				Dim files As FileInfo() = dir.GetFiles(extension, SearchOption.AllDirectories)
				For Each file As FileInfo In files
					Dim fName = file.FullName.Substring(physicalPathLength).Replace("\", "/")
					ads.Add(New BannerDataItem() With { _
					 .ImageUrl = String.Concat(virtualPath, fName), _
					 .AlternateText = file.Name _
					})
				Next
			Next

			Return ads
		End Function
	End Class
End Namespace
````

### Use Custom ItemTemplate

The Rotator provides a built-in ItemTemplate for displaying the images, however in some cases the user would want to modify the HTML of the Rotator’s item. This is done simply, by specifying a new ItemTemplate in the .aspx markup or the code-behind. Here is an example of how this can be done:

````C#
<telerik:RadRotator RenderMode="Lightweight" ID="RadRotator1" runat="server" 
	Width="900px" Height="300px" ItemWidth="300px" ItemHeight="300px"
	BannersPath="~/Images">
	<ItemTemplate>
		<asp:Image ID="Image1" runat="server" ImageUrl='<%# DataBinder.Eval(Container.DataItem, "ImageUrl") %>'
			AlternateText='<%# DataBinder.Eval(Container.DataItem, "AlternateText") %>' />
		<span>Image Name:
			<%# DataBinder.Eval(Container.DataItem, "AlternateText") %>
		</span>
	</ItemTemplate>
</telerik:RadRotator>
````

### Getting Started Tutorial

This tutorial shows how to create a simple web application with RadRotator that animates through a set of images residing into a single directory.

1. Add a RadRotator control on the page and define its dimensions. Also define the dimensions of the items. For the purpose of this demo we set them 300px.

1. Create a directory in the root of your web site and name it “Images”. Place the images you want to rotate in this directory.

1. Set the **BannersPath** property of the rotator to **“~/Images”**. The mark-up should look like the following:

	**ASP.NET**

		<telerik:RadRotator RenderMode="Lightweight" ID="RadRotator1" runat="server"
			Width="600px" Height="300px" ItemWidth="300px" ItemHeight="300px"
			BannersPath="~/Images">
		</telerik:RadRotator> 

1. View the page in the browser, and the Rotator will start animating through the images instantly.

1. In case the images have different width and height than the ones of the RotatorItem, you can easily fix this by placing the following CSS code in the head tag of your page. Note that you must set the CssClass property of the Rotator to RotatorImages. Here is the code:

	**ASP.NET**

		<style type="text/css">
			.RotatorImages .rrBanner
			{
				width: 300px;
				height: 300px;
			}
		</style>

