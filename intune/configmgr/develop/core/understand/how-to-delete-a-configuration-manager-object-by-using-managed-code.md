---
description: Learn how to create a Configuration Manager object by using the managed SMS Provider with WqlConnectionManager.CreateInstance method.
title: "How to Delete a Configuration Manager Object by Using Managed Code"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
---

# How to Delete a Configuration Manager Object by Using Managed Code

To delete a Configuration Manager object by using the managed SMS Provider, use the [IResultObject.Delete](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146496(v=msdn.10)) method. You can get a [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) object for a Configuration Manager object in numerous ways. For more information, see [How to Read a Configuration Manager Object by Using Managed Code](how-to-read-a-configuration-manager-object-by-using-managed-code.md)

### To delete a Configuration Manager object

1. Set up a connection to the SMS Provider. For more information, see [SMS Provider fundamentals](sms-provider-fundamentals.md).
2. Using the `WqlConnectionManager` object you obtain in step one, call the `GetInstance` method to get the `IResultObject` object for the Configuration Manager object.
3. Call the [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) object [Delete](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146496(v=msdn.10)) method to delete the Configuration Manager object.

## Example

The following example deletes a package by using the supplied package identifier. This example uses the **WqlConnectionManager** class **GetInstance** method to get an [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) object for the Configuration Manager package and then deletes the package.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](calling-code-snippets.md).

```
public void DeletePackage(WqlConnectionManager connection, string packageID)
{
    try
    {
        IResultObject package = connection.GetInstance(@"SMS_Package.PackageID='" + packageID + "'");
        package.Delete();
    }
    catch (SmsException ex)
    {
        Console.WriteLine("Failed to delete package: " + ex.Message);
        throw;
    }
}

```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | - **WqlConnectionManager** | A valid connection to the SMS Provider. |
| `PackageID` | - `String` | The package identifier for an existing package. This can be obtained from the [SMS_Package](../../reference/core/servers/configure/sms_package-server-wmi-class.md) class *PackageID* property. |

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

[Objects overview](configuration-manager-objects-overview.md) [How to Call a Configuration Manager Object Class Method by Using Managed Code](how-to-call-a-configuration-manager-object-class-method-by-using-managed-code.md) [How to Connect to a Configuration Manager Provider using Managed Code](how-to-connect-to-an-sms-provider-by-using-managed-code.md) [How to Create a Configuration Manager Object by Using Managed Code](how-to-create-a-configuration-manager-object-by-using-managed-code.md) [How to Modify a Configuration Manager Object by Using Managed Code](how-to-modify-a-configuration-manager-object-by-using-managed-code.md) [How to Perform an Asynchronous Configuration Manager Query by Using Managed Code](how-to-perform-an-asynchronous-query-by-using-managed-code.md) [How to Perform a Synchronous Configuration Manager Query by Using Managed Code](how-to-perform-a-synchronous-configuration-manager-query-by-using-managed-code.md) [How to Read a Configuration Manager Object by Using Managed Code](how-to-read-a-configuration-manager-object-by-using-managed-code.md) [How to Read Lazy Properties by Using Managed Code](how-to-read-lazy-properties-by-using-managed-code.md)
