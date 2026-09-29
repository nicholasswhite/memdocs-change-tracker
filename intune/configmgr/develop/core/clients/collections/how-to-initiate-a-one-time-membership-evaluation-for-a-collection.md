---
title: "How to Initiate a One-time Membership Evaluation for a Collection"
description: "Initiate a One-time Membership Evaluation for a Collection. Get a specific collection instance by using the collection ID provided."  
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3


ms.service: configuration-manager
---

# How to Initiate a One-time Membership Evaluation for a Collection

### To Initiate a One-time Membership Evaluation

1. Set up a connection to the SMS Provider.
2. Get the specific collection instance by using the collection ID provided.
3. Refresh the collection membership using the [RequestRefresh](../../../reference/core/clients/collections/requestrefresh-method-in-class-sms_collection.md) method in the [SMS_Collection](../../../reference/core/clients/collections/sms_collection-server-wmi-class.md) class.

## Example

The following example method refreshes the collection membership for a specific collection.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](../../understand/calling-code-snippets.md).

```vbs
Sub RefreshCollection(connection, collectionID)    Dim collection    Set collection = connection.Get("SMS_Collection.CollectionID='" & collectionID & "'")    Call collection.RequestRefresh()End Sub  
```

```c#
public void RefreshCollection(WqlConnectionManager connection, string collectionID){    IResultObject collection = connection.GetInstance(string.Format("SMS_Collection.CollectionID='{0}'", collectionID));    collection.ExecuteMethod("RequestRefresh", null);}  
```

The example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | - Managed: `WqlConnectionManager` - VBScript: [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) | A valid connection to the SMS Provider. |
| `collectionID` | - Managed: `String` - VBScript: `String` | Unique auto-generated ID containing eight characters. For more information, see the CollectionID property of [SMS_Collection Server WMI Class](../../../reference/core/clients/collections/sms_collection-server-wmi-class.md). |

## Compiling the Code

The C# example requires:

### Namespaces

System

Microsoft.ConfigurationManagement.ManagementProvider

Microsoft.ConfigurationManagement.ManagementProvider.WqlQueryEngine

### Assembly

adminui.wqlqueryengine

microsoft.configurationmanagement.managementprovider

mscorlib

## Robust Programming

For more information about error handling, see [About Configuration Manager Errors](../../understand/about-configuration-manager-errors.md).

## See Also

[SMS_Collection Server WMI Class](../../../reference/core/clients/collections/sms_collection-server-wmi-class.md)
