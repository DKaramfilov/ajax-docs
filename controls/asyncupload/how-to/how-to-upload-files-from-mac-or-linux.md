---
title: How to upload files from MAC or Linux
page_title: How to upload files from MAC or Linux - RadAsyncUpload
description: Check our Web Forms article about How to upload files from MAC or Linux.
slug: asyncupload/how-to/how-to-upload-files-from-mac-or-linux
tags: how,to,upload,files,from,mac,or,linux
published: True
position: 6
---

# How to upload files from MAC or Linux

On some operating systems like MAC OS and Linux it is possible to have file names, which are invalid for the Windows File System, may contain special characters or might not be in accordance with the [Microsoft's Naming Convention.](https://msdn.microsoft.com/en-us/library/windows/desktop/aa365247%28v=vs.85%29.aspx#naming_conventions) This makes file uploading impossible. That's why to upload a file with such invalid name we have to rename it before the uploading. Due to the nature of **AsyncUpload** and due to security restrictions such renaming will require a special way of implementation.

## Uploading files from MAC OS or Linux

* Configure **AsyncUpload** to use a [Custom Handler]({%slug asyncupload/how-to/how-to-extend-the-radasyncupload-handler%})

````ASPNET
<telerik:RadAsyncUpload RenderMode="Lightweight" ID="RadAsyncUpload1" runat="server" HttpHandlerUrl="~/CustomHandler.ashx"  Target="~/Uploads"></telerik:RadAsyncUpload>
<asp:Button ID="btnSubmit" runat="server" Text="Submit Uploaded Files" />
````

* Override the **ChageOriginalFileName** method and perform own file name validation

````C#
<%@ WebHandler Language="C#" Class="CustomHandler" %>

using System;
using System.Web;
using Telerik.Web.UI;
using System.Text.RegularExpressions;
using System.IO;

public class CustomHandler : AsyncUploadHandler
{
    protected override string ChangeOriginalFileName(string fileName)
    {
        return EscapeInvalidCharacter(fileName);
    }

    //Sample escaping of invalid windows characters
    private string EscapeInvalidCharacter(string fileName)
    {
        //Check if there is no invalid characters return the current name
        if (fileName.IndexOfAny(System.IO.Path.GetInvalidFileNameChars()) == -1)
        {
            return fileName;
        }
        else
        {
            //Escape invalid characters
            fileName = Regex.Replace(fileName, @"[^\w\.@-]", "", RegexOptions.None, TimeSpan.FromSeconds(1.5));
            //If all characters are invalid return underscore as a file name
            if (Path.GetFileNameWithoutExtension(fileName).Length == 0)
            {
                return fileName.Insert(0, "_");
            }
            //Else return the escaped name
            return fileName;
        }
    }
}
````
````VB.NET
<%@ WebHandler Language="VB" Class="CustomHandler" %>

Imports System
Imports System.Web
Imports Telerik.Web.UI
Imports System.Text.RegularExpressions
Imports System.IO

Public Class CustomHandler
    Inherits AsyncUploadHandler

    Protected Overrides Function ChangeOriginalFileName(fileName As String) As String
        Return EscapeInvalidCharacter(fileName)
    End Function

    'Sample escaping of invalid windows characters
    Private Function EscapeInvalidCharacter(fileName As String) As String
        'Check if there is no invalid characters return the current name
        If fileName.IndexOfAny(System.IO.Path.GetInvalidFileNameChars()) = -1 Then
            Return fileName
        Else
            'Escape invalid characters
            fileName = Regex.Replace(fileName, "[^\w\.@-]", "", RegexOptions.None, TimeSpan.FromSeconds(1.5))
            'If all characters are invalid return underscore as a file name
            If Path.GetFileNameWithoutExtension(fileName).Length = 0 Then
                Return fileName.Insert(0, "_")
            End If
            'Else return the escaped name
            Return fileName
        End If
    End Function

End Class
````

The solution above results in a red highlighting and no upload of the file, but it does not let the framework know that the filename changed is actually invalid. This extra check can be done like this:

````C#
    protected override bool CheckOriginalFileNameForInvalidChars(string filename)
    {
        return isValid(filename) ... ;
    }
````
````VB.NET
Protected Overrides Function CheckOriginalFileNameForInvalidChars(ByVal filename As String) As Boolean
    Return isValid(filename) ...
End Function
````

You can find more information at [Custom File Name Validation](https://docs.telerik.com/devtools/aspnet-ajax/controls/asyncupload/how-to/how-to-extend-the-radasyncupload-handler#custom-file-name-validation).


# See Also

 * [Custom Handler demo](https://demos.telerik.com/aspnet-ajax/upload/examples/async/imageuploader/defaultcs.aspx?product=asyncupload)
 * [How to Create a Custom Handler for RadAsyncUpload](https://docs.telerik.com/devtools/aspnet-ajax/controls/asyncupload/how-to/how-to-extend-the-radasyncupload-handler)
