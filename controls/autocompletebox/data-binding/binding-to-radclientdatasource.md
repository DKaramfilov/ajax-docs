---
title: Binding to RadClientDataSource
page_title: Binding to RadClientDataSource - RadAutoCompleteBox
description: Check our Web Forms article about Binding to RadClientDataSource.
slug: autocompletebox/data-binding/binding-to-radclientdatasource
tags: binding,to,radclientdatasource
published: True
position: 7
---

# Binding to RadClientDataSource



This article demonstrates how to bind **RadAutoCompleteBox** to **RadClientDataSource**.

## 

Since **Q2 2014** RadAutoCompleteBox can be bound to a **RadClientDataSource** control. An important aspect of binding to the RadClientDataSource is that the RadAutoCompleteBox **DataText** and **DataValue** fields should be associated with the custom object properties. Thus you can choose which property value to be shown as RadAutoCompleteBox item text and value. For reference at the bottom of the web service implementation below you will find the custom class and its properties declaration.

The RadAutoCompleteBox property **MaxResultCount** works in exactly the same manner as with any other data source control.

## 

The following application scenario shows an example of RadAutoCompleteBox bound to RadClientDataSource.

````ASPNET
<telerik:RadClientDataSource runat="server" ID="CD1">
	<ClientEvents />
	<DataSource>
		<WebServiceDataSourceSettings BaseUrl="LoadEntriesWCF.svc/">
			<Select Url="LoadCustomDataWCF" DataType="JSON" RequestType="Post" ContentType="application/json; charset=utf-8" />
		</WebServiceDataSourceSettings>
	</DataSource>

	<Schema DataName="d">
	</Schema>
	<ClientEvents />
</telerik:RadClientDataSource>

<telerik:RadAutoCompleteBox RenderMode="Lightweight" ID="RadAutoCompleteBox1" Filter="StartsWith" ShowLoadingIcon="true" runat="server" Width="500" DropDownHeight="150"
	MaxResultCount="2"
	DataTextField="Name"
	DataValueField="Value"
	ClientDataSourceID="CD1"
	DropDownWidth="250">
</telerik:RadAutoCompleteBox>
````





````C#
[OperationContract]
public CustomData[] LoadCustomDataWCF()
{
	NorthwindReadOnlyDataContext northwind = new NorthwindReadOnlyDataContext();

	//Get all items from the Customers table. This query will not be executed untill the ToArray method is called.
	var allCustomers = (from customer in northwind.Customers
						orderby customer.ContactName
						select new CustomData
						{
							Name = customer.ContactName,
							Value = customer.CustomerID
						}).Take<CustomData>(46);

	var result = allCustomers.ToArray();

	return result;
}
public class CustomData
{
	public string Name { get; set; }
	public string Value { get; set; }

}
````
````VB.NET
Inherits System.Web.UI.Page
<OperationContract> _
Public Function LoadCustomDataWCF() As CustomData()
	Dim northwind As New NorthwindReadOnlyDataContext()

	'Get all items from the Customers table. This query will not be executed untill the ToArray method is called.
Dim allCustomers = (From customer In northwind.CustomersOrder By customer.ContactNameNew CustomData() With { _
	Key .Name = customer.ContactName, _
	Key .Value = customer.CustomerID _
}).Take(Of CustomData)(46)

	Dim result = allCustomers.ToArray()

	Return result
End Function

 Public Class CustomData
	Public Property Name() As String
		Get
			Return m_Name
		End Get
		Set(value As String)
			m_Name = Value
		End Set
	End Property
	Private m_Name As String
	Public Property Value() As String
		Get
			Return m_Value
		End Get
		Set(value As String)
			m_Value = Value
		End Set
	End Property
	Private m_Value As String

End Class
````


