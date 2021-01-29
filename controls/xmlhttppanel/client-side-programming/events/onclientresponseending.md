---
title: OnClientResponseEnding
page_title: OnClientResponseEnding - RadXmlHttpPanel
description: Check our Web Forms article about OnClientResponseEnding.
slug: xmlhttppanel/client-side-programming/events/onclientresponseending
tags: onclientresponseending
published: True
position: 2
---

# OnClientResponseEnding





The **OnClientResponseEnding** client-side event replaces the existing **OnClientResponseEnd** client-side event . Please note that although the **OnClientResponseEnding** should be used from now on, the **OnClientResponseEnd** is still present in the control’s API so that any existing applications are not broken after an upgrade to a newer version of the control.

The **OnClientResponseEnding** occurs before the data (content) is pasted into the RadXmlHttpPanel, after a partial update request has been initiated by the **RadXmlHttpPanel** `set_value` method.

The event handler receives two parameters:

1. The instance of the **RadXmlHttpPanel** control firing the event.

1. An eventArgs parameter containing the following properties and methods:

	1. `set_cancel` lets you prevent from loading the content inside the RadXmlHttpPanel and raising the OnClientResponseEnded client-side event.
	
	1. `get_cancel` returns a boolean value indicating whether the RadXmlHttpPanel’s content update was canceled.
	
	1. `get_content` gets the HTML content rendered inside the RadXmlHttpPanel.

The following example demonstrates how you can cancel the loading of the content inside the **RadXmlHttpPanel**. An event handler should be provided for the **OnClientResponseEnding** client-side event where the action can be canceled by using the cancel property of the eventArgs passed to the handler

````JavaScript
function SetValue()
{
    var panel = $find("<%= RadXmlHttpPanel1.ClientID %>");
    var value = "some_value";
    panel.set_value(value);
}
function OnClientResponseEnding(panel, args)
{
    var result = confirm("Do not load the content in the XmlPanel?");
    args.set_cancel(result);
}
````





````ASP.NET
<input type="button" value="Refresh RadXmlHttpPanel1" onclick="SetValue()" />
<telerik:RadXmlHttpPanel ID="RadXmlHttpPanel1" runat="server" OnServiceRequest=" RadXmlHttpPanel1_ServiceRequest"
    OnClientResponseEnding="OnClientResponseEnding">
    <telerik:RadGrid RenderMode="Lightweight" ID="RadGrid1" RegisterWithScriptManager="false" ID="RadGridTeamPlayer"
        runat="server" AllowSorting="False" AutoGenerateColumns="True" GridLines="Both"
        Height="100%" ShowFooter="false" Style="border: solid 1px black; outline: 0">
        <MasterTableView>
            <Columns>
                <telerik:GridBoundColumn DataField="username" HeaderText="Player" SortExpression="username">
                    <ItemStyle HorizontalAlign="center" />
                    <HeaderStyle HorizontalAlign="center" />
                </telerik:GridBoundColumn>
            </Columns>
        </MasterTableView>
    </telerik:RadGrid>
</telerik:RadXmlHttpPanel>
````





````C#
protected void RadXmlHttpPanel1_ServiceRequest(object sender, Telerik.Web.UI.RadXmlHttpPanelEventArgs e)
{
	string val = e.Value; BindGrid(val);
}
void BindGrid(string parametervalue)
{
	RadGrid1.DataSource = new string[] { "1", "2", DateTime.Now.ToLongTimeString() };
	RadGrid1.DataBind();
}
````
````VB
Protected Sub RadXmlHttpPanel1_ServiceRequest(ByVal sender As Object, ByVal e As RadXmlHttpPanelEventArgs)
    Dim val As String = e.Value
    BindGrid(val)
End Sub

Sub BindGrid(ByVal parametervalue As String)
    RadGrid1.DataSource = New String() {"1", "2", DateTime.Now.ToLongTimeString()}
    RadGrid1.DataBind()
End Sub
````

