---
title: Binding to RadClientDataSource
page_title: Binding to RadClientDataSource - RadDataForm
description: Check our Web Forms article about Binding to RadClientDataSource.
slug: dataform/data-binding/binding-to-radclientdatasource
tags: binding,to,radclientdatasource
published: True
position: 2
---

# Binding to RadClientDataSource



Since Q1 2015 **RadDataForm** supports client-side data binding. The following article describes how you can bind the control using **RadClientDataSource**.

## Binding to RadClientDataSource

You need to ensure that the templates relevant to your scenario are defined for **RadDataForm**.The **ItemTemplate** is used to preview data. **EditItemTemplate** will be used in edit mode and **InsertItemTemplate** when inserting data.

The key when implementing **RadDataForm** with client-side binding is to handle the **GetValues** and **SetValues** client events. In addition you need to ensure that the **ClientDataSourceID** is set to the **ID** of a **RadClientDataSource** control.

The **SetValues** event should be used to set the values for the fields in preview mode. In the **GetValue** handler you should get the values that are entered by the user.

## Example

The following example outlines how you can bind the **RadDataForm** to **RadClientDataSource**.



````ASPNET	
<telerik:RadDataForm RenderMode="Lightweight" runat="server" ID="RadDataForm1"
    DataKeyNames="CustomerID" RenderWrapper="true" class="rdfRightAligned rdfNoFieldHint rdfNoFieldHint" ClientDataSourceID="RadClientDataSource1">
    <clientsettings>
        <ClientEvents OnSetValues="dataFormSetValues" OnGetValues="dataFormGetValues" OnDataFormCreated="dataFormCreated" />
    </clientsettings>
    <LayoutTemplate>
        <div style="width: 531px" class="RadDataForm RadDataForm_<%# Container.Skin %> rdfRightAligned rdfNoFieldHint rdfNoFieldHint">
            <div id="itemPlaceholder" runat="server">
            </div>
            <div class="rdfPager rdfPagerRight">
                <span>
                    <asp:Button ID="btnFirst" OnClientClick="dataform1.page('First'); return false;" runat="server" CssClass="rdfFirst" Text=" " ToolTip="First" />
                    <asp:Button ID="btnPrev" OnClientClick="dataform1.page('Prev'); return false;" runat="server" CssClass="rdfPrev" Text=" " ToolTip="Previous" />
                </span><span>
                    <asp:Button ID="btnNext" OnClientClick="dataform1.page('Next'); return false;" runat="server" CssClass="rdfNext" Text=" " ToolTip="Next" />
                    <asp:Button ID="btnLast" OnClientClick="dataform1.page('Last'); return false;" runat="server" CssClass="rdfLast" Text=" " ToolTip="Last" />
                </span>
            </div>
        </div>
    </LayoutTemplate>
    <ItemTemplate>
        <fieldset id="View" class="rdfFieldset rdfBorders">
            <legend class="rdfLegend">Customers</legend>
            <div class="rdfRow">
                <asp:Label ID="ViewCustomerIDLabel2" runat="server" CssClass="rdfLabel" Text="Customer ID:"></asp:Label>
                <asp:Label ID="ViewCustomerIDLabel1" runat="server" CssClass="rdfFieldValue" Text='' />
            </div>
            <div class="rdfRow">
                <asp:Label ID="ViewCompanyNameLabel2" runat="server" CssClass="rdfLabel" Text="Company Name:"></asp:Label>
                <asp:Label ID="ViewCompanyNameLabel1" runat="server" CssClass="rdfFieldValue" Text='' />
            </div>
            <div class="rdfRow">
                <asp:Label ID="ViewContactNameLabel2" runat="server" CssClass="rdfLabel" Text="Contact Name:"></asp:Label>
                <asp:Label ID="ViewContactNameLabel1" runat="server" CssClass="rdfFieldValue" Text='' />
            </div>
            <div class="rdfRow">
                <asp:Label ID="ViewContactTitleLabel2" runat="server" CssClass="rdfLabel" Text="Contact Title:"></asp:Label>
                <asp:Label ID="ViewContactTitleLabel1" runat="server" CssClass="rdfFieldValue" Text='' />
            </div>

            <div class="rdfCommandButtons">
                <hr class="rdfHr" />
                <telerik:RadButton RenderMode="Lightweight" ID="InitInsertButton" runat="server" ButtonType="SkinnedButton" OnClientClicked="function(){dataform1.showInsertItem();}" AutoPostBack="false" Text="Insert" ToolTip="Insert" />
                <telerik:RadButton RenderMode="Lightweight" ID="EditButton" runat="server" ButtonType="SkinnedButton" OnClientClicked="function(){dataform1.editItem();}" AutoPostBack="false" Text="Edit" ToolTip="Edit" />
                <telerik:RadButton RenderMode="Lightweight" ID="DeleteButton" runat="server" ButtonType="SkinnedButton" CausesValidation="False"
                    CommandName="Delete" CommandArgument='<%#Eval("ProductID") %>'
                    OnClientClicking='function(sender, args){args.set_cancel(!window.confirm("Are you sure you want to delete this record?"));}'
                    Text="Delete" ToolTip="Delete" />
            </div>
        </fieldset>
    </ItemTemplate>
    <EditItemTemplate>
        <fieldset id="Edit" class="rdfFieldset rdfBorders">
            <legend class="rdfLegend">Edit Customers</legend>
            <div class="rdfRow">
                <asp:Label ID="EditCustomerIDLabel2" runat="server" CssClass="rdfLabel" Text="Product ID:"></asp:Label>
                <asp:Label ID="EditCustomerIDLabel1" runat="server" CssClass="rdfFieldValue" />
            </div>

            <div class="rdfRow">
                <asp:Label ID="EditCompanyNameLabel" runat="server" AssociatedControlID="EditCompanyName" CssClass="rdfLabel" Text="Company Name:"></asp:Label>
                <telerik:RadTextBox RenderMode="Lightweight" ID="EditCompanyName" runat="server" Text='' WrapperCssClass="rdfInput" />
            </div>
            <div class="rdfRow">
                <asp:Label ID="EditContactNameLabel" runat="server" AssociatedControlID="EditContactName" CssClass="rdfLabel" Text="Contact Name:"></asp:Label>
                <telerik:RadTextBox RenderMode="Lightweight" ID="EditContactName" runat="server" WrapperCssClass="rdfInput" />
            </div>
            <div class="rdfRow">
                <asp:Label ID="EditContactTitlelabel" runat="server" AssociatedControlID="EditContactTitle" CssClass="rdfLabel" Text="Contact Title:"></asp:Label>
                <telerik:RadTextBox RenderMode="Lightweight" ID="EditContactTitle" runat="server" WrapperCssClass="rdfInput" />
            </div>

            <div class="rdfCommandButtons">
                <hr class="rdfHr" />
                <telerik:RadButton RenderMode="Lightweight" ID="UpdateButton" runat="server" ButtonType="SkinnedButton" CommandName="Update" Text="Update" ToolTip="Update" />
                <telerik:RadButton RenderMode="Lightweight" ID="CancelButton" runat="server" ButtonType="SkinnedButton" CausesValidation="False" CommandName="Cancel" Text="Cancel" ToolTip="Cancel" />
            </div>
        </fieldset>
    </EditItemTemplate>
    <InsertItemTemplate>
        <fieldset id="Insert" class="rdfFieldset rdfBorders">
            <legend class="rdfLegend">Insert New Customers</legend>
            <div class="rdfRow">
                <asp:Label ID="ProductNameLabel2" runat="server" AssociatedControlID="InsertCompanyName" CssClass="rdfLabel" Text="Company Name:"></asp:Label>
                <telerik:RadTextBox RenderMode="Lightweight" ID="InsertCompanyName" runat="server" Text='' WrapperCssClass="rdfInput" />
            </div>
            <div class="rdfRow">
                <asp:Label ID="Label1" runat="server" AssociatedControlID="InsertContactName" CssClass="rdfLabel" Text="Contact Name:"></asp:Label>
                <telerik:RadTextBox RenderMode="Lightweight" ID="InsertContactName" runat="server" WrapperCssClass="rdfInput" />
            </div>
            <div class="rdfRow">
                <asp:Label ID="Label2" runat="server" AssociatedControlID="InsertContactTitle" CssClass="rdfLabel" Text="Contact Title:"></asp:Label>
                <telerik:RadTextBox RenderMode="Lightweight" ID="InsertContactTitle" runat="server" WrapperCssClass="rdfInput" />
            </div>

            <div class="rdfCommandButtons">
                <hr class="rdfHr" />
                <telerik:RadButton RenderMode="Lightweight" ID="PerformInsertButton" runat="server" ButtonType="SkinnedButton" OnClientClicked="function(){dataform1.insertItem();}" AutoPostBack="false" Text="Insert" ToolTip="Insert" />
                <telerik:RadButton RenderMode="Lightweight" ID="CancelButton" runat="server" ButtonType="SkinnedButton" OnClientClicked="function(){dataform1.cancelInsert();}" AutoPostBack="false" Text="Cancel" ToolTip="Cancel" />
            </div>
        </fieldset>
    </InsertItemTemplate>
</telerik:RadDataForm>

<telerik:RadClientDataSource ID="RadClientDataSource1" runat="server" AllowBatchOperations="true">
    <ClientEvents OnCustomParameter="ParameterMap" OnDataParse="Parse" />
    <DataSource>
        <WebServiceDataSourceSettings BaseUrl="EditingWcfService.svc/">
            <Select Url="GetCustomers" DataType="JSON" />
            <Update Url="UpdateCustomers" DataType="JSON" />
            <Insert Url="InsertCustomers" DataType="JSON" />
            <Delete Url="DeleteCustomers" DataType="JSON" />
        </WebServiceDataSourceSettings>
    </DataSource>
    <Schema>
        <Model ID="CustomerID">
            <telerik:ClientDataSourceModelField FieldName="CustomerID" DataType="String" />
            <telerik:ClientDataSourceModelField FieldName="CompanyName" DataType="String" />
            <telerik:ClientDataSourceModelField FieldName="ContactName" DataType="String" />
            <telerik:ClientDataSourceModelField FieldName="ContactTitle" DataType="String" />
        </Model>
    </Schema>
</telerik:RadClientDataSource>	
````
````JavaScript
<script type="text/javascript">
    function ParameterMap(sender, args) {
        if (args.get_type() != "read" && args.get_data()) {
            args.set_parameterFormat({ customersJSON: kendo.stringify(args.get_data().models) });
        }
    }
    function Parse(sender, args) {
        var response = args.get_response().d;
        if (response) {
            args.set_parsedData(response.Data);
        }
    }

    function dataFormCreated(sender, args) {
        window.dataform1 = sender;
    }

    function dataFormSetValues(sender, args) {
        var dataItem = args;
        $telerik.findElement(document, "ViewCustomerIDLabel1").innerHTML = dataItem.CustomerID;
        $telerik.findElement(document, "ViewCompanyNameLabel1").innerHTML = dataItem.CompanyName;
        $telerik.findElement(document, "ViewContactNameLabel1").innerHTML = dataItem.ContactName;
        $telerik.findElement(document, "ViewContactTitleLabel1").innerHTML = dataItem.ContactTitle;
    }

    function dataFormGetValues(sender, args) {

        if (args.get_commandName() == "PerformInsert") {
            var dataItem = {};
            dataItem.CompanyName = $telerik.findControl(document, "InsertCompanyName").get_value();
            dataItem.ContactName = $telerik.findControl(document, "InsertContactName").get_value();
            dataItem.ContactTitle = $telerik.findControl(document, "InsertContactTitle").get_value();
            args.set_dataItem(dataItem);
        }
    }
</script>
````

