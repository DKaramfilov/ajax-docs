---
title: Configure RadFileExplorer on the Server
page_title: Configure RadFileExplorer on the Server - RadFileExplorer
description: Check our Web Forms article about Configure RadFileExplorer on the Server.
slug: fileexplorer/server-side-programming/configure-radfileexplorer-on-the-server
tags: configure,radfileexplorer,on,the,server
published: True
position: 2
---

# Configure RadFileExplorer on the Server

For convenience the subcontrols of **RadFileExplorer** (RadMenu, RadUpload, etc.) are exposed so developers could change their look or behavior, however the configuration of the RadFileExplorer itself is done in **RadFileExplorer.Configuration**.

````C#
protected void Page_Load(object sender, EventArgs e)
{
	string[] paths = new string[] { "~/" };
	// This code sets RadFileExplorer's paths
	RadFileExplorer1.Configuration.ViewPaths = paths;
	RadFileExplorer1.Configuration.UploadPaths = paths;
	RadFileExplorer1.Configuration.DeletePaths = paths;

	// Sets Max file size
	RadFileExplorer1.Configuration.MaxUploadFileSize = 10485760;

	// Enables Paging on the Grid
	RadFileExplorer1.AllowPaging = true;
	// Sets the page size
	RadFileExplorer1.PageSize = 20;

	//Load the default FileSystemContentProvider
	RadFileExplorer1.Configuration.ContentProviderTypeName = 
		typeof(Telerik.Web.UI.Widgets.FileSystemContentProvider).AssemblyQualifiedName;
}
````
````VB
Protected Sub Page_Load(ByVal sender As Object, ByVal e As System.EventArgs) Handles Me.Load
	Dim paths As String() = New String() {"~/"}
	'This code sets RadFileExplorer's paths
	RadFileExplorer1.Configuration.ViewPaths = paths
	RadFileExplorer1.Configuration.UploadPaths = paths
	RadFileExplorer1.Configuration.DeletePaths = paths

	'Sets Max file size
	RadFileExplorer1.Configuration.MaxUploadFileSize = 10485760

	' Enables Paging on the Grid
	RadFileExplorer1.AllowPaging = True
	' Sets the page size
	RadFileExplorer1.PageSize = 20

	'Load the default FileSystemContentProvider
	RadFileExplorer1.Configuration.ContentProviderTypeName = 
		GetType(Telerik.Web.UI.Widgets.FileSystemContentProvider).AssemblyQualifiedName

End Sub
````

## See Also

 * [FileExplorerControls Enumeration](https://www.telerik.com/help/aspnet-ajax/t_telerik_web_ui_fileexplorer_fileexplorercontrols.html)

 * [RadFileExplorer Class Members](https://www.telerik.com/help/aspnet-ajax/allmembers_t_telerik_web_ui_radfileexplorer.html)

 * [RadFileExplorer ItemCommand Event](https://www.telerik.com/help/aspnet-ajax/e_telerik_web_ui_radfileexplorer_itemcommand.html)
