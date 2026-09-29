---
title: "How to Perform a Synchronous Configuration Manager Query by Using Managed Code"
description: To perform a synchronous query by using the managed SMS Provider, you use *WqlConnectionManager.QueryProcessor.ExecuteQuery* method.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
---

# How to Perform a Synchronous Configuration Manager Query by Using Managed Code

To perform a synchronous query by using the managed SMS Provider, you use *WqlConnectionManager.QueryProcessor.ExecuteQuery* method.

The [ExecuteQuery](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146278(v=msdn.10)) method takes a WQL query string and optional context information for the call. An [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) is returned containing the objects found in the query.

### To perform a synchronous query

1. Set up a connection to the SMS Provider. For more information, see [SMS Provider fundamentals](sms-provider-fundamentals.md).
2. Using the **WqlConnectionManager** object you obtain in step one, call the **QueryProcessor** object *ExecuteQuery* method to query SMS Provider and get an [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) containing a collection of query results.

## Example

The following code example shows how to make a synchronous query for the available packages by using *ExecuteQuery*.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](calling-code-snippets.md).

```
public void QueryPackages(WqlConnectionManager connection)
{
    try
    {
        IResultObject query = connection.QueryProcessor.ExecuteQuery("Select * from SMS_Package");
        foreach (IResultObject o in query)
        {
            Console.WriteLine(o["Name"].StringValue);
            o.Dispose();
        }
    }
    catch (SmsException ex)
    {
        Console.WriteLine("Failed to query packages: " + ex.Message);
        throw;
    }
}

```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | Managed: `WqlConnectionManager` | A valid connection to the SMS Provider. |

## Compiling the Code

### Namespaces

System

System.Collections.Generic

System.ComponentModel

Microsoft.ConfigurationManagement.ManagementProvider

Microsoft.ConfigurationManagement.ManagementProvider.WqlQueryEngine

### Assembly

microsoft.configurationmanagement.managementprovider

adminui.wqlqueryengine

## Robust Programming

The Configuration Manager exceptions that can be raised are [SmsConnectionException](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147431(v=msdn.10)) and [SmsQueryException](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147436(v=msdn.10)). These can be caught together with [SmsException](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147433(v=msdn.10)).

## See Also

[Objects overview](configuration-manager-objects-overview.md) [Configuration Manager Lazy Properties](configuration-manager-lazy-properties.md) [How to Call a Configuration Manager Object Class Method by Using Managed Code](how-to-call-a-configuration-manager-object-class-method-by-using-managed-code.md) [How to Connect to a Configuration Manager Provider using Managed Code](how-to-connect-to-an-sms-provider-by-using-managed-code.md) [How to Create a Configuration Manager Object by Using Managed Code](how-to-create-a-configuration-manager-object-by-using-managed-code.md) [How to Modify a Configuration Manager Object by Using Managed Code](how-to-modify-a-configuration-manager-object-by-using-managed-code.md) [How to Perform an Asynchronous Configuration Manager Query by Using Managed Code](how-to-perform-an-asynchronous-query-by-using-managed-code.md) [How to Read a Configuration Manager Object by Using Managed Code](how-to-read-a-configuration-manager-object-by-using-managed-code.md) [How to Read Lazy Properties by Using Managed Code](how-to-read-lazy-properties-by-using-managed-code.md) [Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md) [Configuration Manager Result Sets](result-sets.md) [Configuration Manager Special Queries](special-queries.md) [About queries](about-configuration-manager-queries.md)
