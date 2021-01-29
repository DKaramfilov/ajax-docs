---
title: Telerik.Web.UI.RadClientDataSource
description: Telerik.Web.UI.RadClientDataSource
slug: Telerik.Web.UI.RadClientDataSource
---

# Telerik.Web.UI.RadClientDataSource : Sys.Component 

## Inheritance Hierarchy

* Sys.Component
* *[Telerik.Web.UI.RadClientDataSource]({%slug Telerik.Web.UI.RadClientDataSource%})*


## Methods

### add

Appends a data item to the data source.

#### Parameters

##### values `Object`

JSON formated values to insert as a new item

#### Returns

`None` 

### aggregates

A method to returned the calculated aggregate values of the RadClientDataSource

#### Parameters

#### Returns

`Object` Returns the aggregated values of the RadClientDataSource

### cancelChanges

Cancels any pending changes in the data source. Used with batch editing

#### Parameters

#### Returns

`None` 

### fetch

Method which return data from the web service after calling the select method from the transport settings

#### Parameters

##### callback `Function`

the callback function that will hold the returned data

#### Returns

`None` 

### get_aggregates

Gets the collection of Telerik.Web.UI.ClientDataSourceAggregate in RadClientDataSource.

#### Parameters

#### Returns

`Telerik.Web.UI.ClientDataSource.AggregateCollection`  The collection of Telerik.Web.UI.ClientDataSourceAggregate items which are part of the RadClientDataSource. 

### get_allowBatchOperations

Gets the RadClientDataSource.AllowBatchOperations value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.AllowBatchOperations value.

### get_allowPaging

Gets the RadClientDataSource.AllowPaging value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.AllowPaging value.

### get_currentPageIndex

Gets the RadClientDataSource.CurrentPageIndex value.

#### Parameters

#### Returns

`Number` The RadClientDataSource.CurrentPageIndex value.

### get_data

Gets the JSON data of the RadClientDataSource

#### Parameters

#### Returns

`Object` The data of the RadClientDataSource

### get_dataSourceObject

Gets the kendoDataSource underlying widget. 
To use the exposed Kendo methods make sure you have the kendo.dataviz.d.ts file and cast the returned object to kendo.data.DataSource.

#### Parameters

#### Returns

`Object` The Kendo DataSource instance.

### get_enableServerAggregates

Gets the RadClientDataSource.EnableServerAggregates value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerAggregates value.

### get_enableServerFiltering

Gets the RadClientDataSource.EnableServerFiltering value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerFiltering value.

### get_enableServerGrouping

Gets the RadClientDataSource.EnableServerGrouping value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerGrouping value.

### get_enableServerPaging

Gets the RadClientDataSource.EnableServerPaging value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerPaging value.

### get_enableServerSorting

Gets the RadClientDataSource.EnableServerSorting value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerSorting value.

### get_filterExpressions

Gets the collection of Telerik.Web.UI.ClientDataSourceFilterExpression in RadClientDataSource.

#### Parameters

#### Returns

`Telerik.Web.UI.ClientDataSource.FilterExpressionCollection`  The collection of Telerik.Web.UI.ClientDataSourceFilterExpression items which are part of the RadClientDataSource. 

### get_groupExpressions

Gets the collection of Telerik.Web.UI.ClientDataSource.GroupExpression in RadClientDataSource.

#### Parameters

#### Returns

`Telerik.Web.UI.ClientDataSource.GroupExpressionCollection`  The collection of Telerik.Web.UI.ClientDataSource.GroupExpression items which are part of the RadClientDataSource. 

### get_pageSize

Gets the RadClientDataSource.PageSize value.

#### Parameters

#### Returns

`Number` The RadClientDataSource.PageSize value.

### get_schema

Gets the RadClientDataSource.Schema value.

#### Parameters

#### Returns

`Telerik.Web.UI.ClientDataSourceSchema` The RadClientDataSource.Schema value.

### get_sortExpressions

Gets the collection of Telerik.Web.UI.ClientDataSourceSortExpression in RadClientDataSource.

#### Parameters

#### Returns

`Telerik.Web.UI.ClientDataSource.SortExpressionCollection`  The collection of Telerik.Web.UI.ClientDataSource.SortExpression items which are part of the RadClientDataSource. 

### get_totalItemsCount

Gets the total number of items in the RadClientDataSource

#### Parameters

#### Returns

`Number` The total number of items in the RadClientDataSource.

### get_totalPagesCount

Gets the total number of pages in the RadClientDataSource

#### Parameters

#### Returns

`Number` The total number of pages in the RadClientDataSource.

### get_transport

Gets the RadClientDataSource.DataSource.WebServiceDataSourceSettings value.

#### Parameters

#### Returns

`Telerik.Web.UI.DataSourceSettings.WebServiceDataSourceSettings` The RadClientDataSource.DataSource.WebServiceDataSourceSettings value.

### getDataItemById

Gets the data item with the specified model id.

#### Parameters

#### Returns

`None` 

### getItemByIndex

Returns the data item at the specified index.

#### Parameters

#### Returns

`None` 

### hasChanges

Checks if the data items have changed.

#### Parameters

#### Returns

`None` 

### insert

Inserts a data item in the data source at the specified index.

#### Parameters

##### index `Number`

the index at which the item will be inserted

#### Returns

`None` 

### Method

Parameters

#### Parameters

##### Description `Object`

#### Returns

`None` 

### remove

Removes the specified data item from the data source.

#### Parameters

#### Returns

`None` 

### set_allowBatchOperations

Sets the RadClientDataSource.AllowBatchOperations value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.AllowBatchOperations value.

### set_allowPaging

Sets the RadClientDataSource.AllowPaging value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.AllowPaging value.

### set_currentPageIndex

Sets the RadClientDataSource.CurrentPageIndex value.

#### Parameters

#### Returns

`Number` The RadClientDataSource.CurrentPageIndex value.

### set_data

Sets the JSON data of the RadClientDataSource

#### Parameters

#### Returns

`None` 

### set_enableServerAggregates

Sets the RadClientDataSource.EnableServerAggregates value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerAggregates value.

### set_enableServerFiltering

Sets the RadClientDataSource.EnableServerFiltering value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerFiltering value.

### set_enableServerGrouping

Sets the RadClientDataSource.EnableServerGrouping value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerGrouping value.

### set_enableServerPaging

Sets the RadClientDataSource.EnableServerPaging value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerPaging value.

### set_enableServerSorting

Sets the RadClientDataSource.EnableServerSorting value.

#### Parameters

#### Returns

`Boolean` The RadClientDataSource.EnableServerSorting value.

### set_pageSize

Sets the RadClientDataSource.PageSize value.

#### Parameters

#### Returns

`Number` The RadClientDataSource.PageSize value.

### sync

Persists any data item changes to the datasource. Calls the respective CRUd methods from the transport

#### Parameters

#### Returns

`None` 

### update

updates the values of the items with the specified model id

#### Parameters

##### newValues `Object`

JSON formated values to update in the item

#### Returns

`None` 

### view

Returns the data items which correspond to the current page, filter, sort and group configuration.

#### Parameters

#### Returns

`None` 


## Events

### dataRequested

Raised after the data has been requested from the service.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### sync

Raised after the data source saves data item changes. The data source saves the data item changes when the sync method is called.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### dataParse

Can be used to additionally parse the response before it is further processed by the control.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### change

Raised when a change in the data is applied.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### customParameter

Raised when a custom mapping of the request parameters can be performed.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### command

Raised when a RadClientDataSource command occurs.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.CancelEventArgs`

### requestEnd

Raised when a RadClientDataSource remote request finished.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### requestStart

Raised when a RadClientDataSource remote service or page request is started.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`

### requestFailed

Raised when the remote request has failed.

#### Event Data

##### sender `Telerik.Web.UI.RadClientDataSource`

The RadClientDataSource control that raised the event

##### args `Sys.EventArgs`


