---
title: Prevent Dual File Uploading
page_title: Prevent Dual File Uploading - RadCloudUpload
description: Check our Web Forms article about Prevent Dual File Uploading.
slug: cloudupload/how-to/prevent-dual-file-uploading
tags: prevent,dual,file,uploading
published: True
position: 4
---

# Prevent Dual File Uploading



This article shows step by step how to prevent dual uploading of a file which has already been uploaded.

## Prevent Dual Files Uploading

1. Add new **RadCloudUpload** control.

1. Handle [ OnClientFileUploading ]({%slug cloudupload/client-side-programming/events/onclientfileuploading%})



````ASPNET
<telerik:RadCloudUpload ID="RadCloudUpload1" runat="server" ProviderType="Azure" OnClientFileUploading="onClientFileUploading" MultipleFileSelection="Automatic">
</telerik:RadCloudUpload>
````

````JavaScript
//Prevent uploading of file, which has already been uploaded.
function onClientFileUploading(sender, args) {
	var fileName = args.get_fileName();
	var uploadedFiles = sender.get_uploadedFiles();
	for (var i = 0; i < uploadedFiles.length; i++) {
		if (uploadedFiles[i].originalFileName === fileName) {
			args.set_cancel(true);
			alert(fileName + ' has already been uploaded.');
		}
	}
}
````


# See Also

 * [Troubleshooting]({%slug cloudupload/troubleshooting%})
