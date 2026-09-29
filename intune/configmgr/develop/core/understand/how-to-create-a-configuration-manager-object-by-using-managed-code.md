---
title: "How to Create a Configuration Manager Object by Using Managed Code"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
description: Learn how to create a configuration manager object by using managed code, with included examples and links.
ms.service: configuration-manager
---

# How to Create a Configuration Manager Object by Using Managed Code

To create a Configuration Manager object by using the managed SMS Provider, use *WqlConnectionManager.CreateInstance* method. The [ConnectionManagerBase.CreateInstance](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146180(v=msdn.10)) method takes the required object type as a string parameter and returns an [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) object that is used to populate the new object. The [IResultObject.Put](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146500(v=msdn.10)) method must be called to submit the object to the SMS Provider.

### To create a Configuration Manager object

1. Set up a connection to the SMS Provider. For more information, see [SMS Provider fundamentals](sms-provider-fundamentals.md).
2. Using the **WqlConnectionManager** connection object you obtain in step one, call **[CreateInstance** to create the required the WMI object, and receive its IResultObject object instance.
3. Populate the [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) properties.
4. Commit the **IResultObject** to the SMS Provider.

## Example

The following example demonstrates how to create and then populate a new Configuration Manager package (`SMS_Package`).

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](calling-code-snippets.md).

```csharp
public void CreatePackage(WqlConnectionManager connection)
{
    try
    {
        IResultObject package = connection.CreateInstance("SMS_Package");
        package["Name"].StringValue = "Test Package";
        package["Description"].StringValue = "A test package";
        package["PkgSourcePath"].StringValue = @"c:\Package Source";

        package.Put();
    }

    catch (SmsException ex)
    {
        Console.WriteLine("Failed to create package. Error: " + ex.Message);
        throw;
    }
}

```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | Managed: **WqlConnectionManager** | A valid connection to the SMS Provider. |

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

[Objects overview](configuration-manager-objects-overview.md)

[Configuration Manager Lazy Properties](configuration-manager-lazy-properties.md)

[How to Call a Configuration Manager Object Class Method by Using Managed Code](how-to-call-a-configuration-manager-object-class-method-by-using-managed-code.md)

[How to Connect to a Configuration Manager Provider using Managed Code](how-to-connect-to-an-sms-provider-by-using-managed-code.md)

[How to Modify a Configuration Manager Object by Using Managed Code](how-to-modify-a-configuration-manager-object-by-using-managed-code.md)

[How to Perform an Asynchronous Configuration Manager Query by Using Managed Code](how-to-perform-an-asynchronous-query-by-using-managed-code.md)

[How to Perform a Synchronous Configuration Manager Query by Using Managed Code](how-to-perform-a-synchronous-configuration-manager-query-by-using-managed-code.md)

[How to Read a Configuration Manager Object by Using Managed Code](how-to-read-a-configuration-manager-object-by-using-managed-code.md)

[How to Read Lazy Properties by Using Managed Code](how-to-read-lazy-properties-by-using-managed-code.md)
