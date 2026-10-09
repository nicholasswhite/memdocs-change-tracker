---
title: "How to Perform a Synchronous Configuration Manager Query by Using WMI"
description: In Configuration Manager, you perform a synchronous query for Configuration Manager objects by calling the SWbemServices object ExecQuery method and passing a WQL query.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# How to Perform a Synchronous Configuration Manager Query by Using WMI

In Configuration Manager, you perform a synchronous query for Configuration Manager objects by calling the [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) object [ExecQuery](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices-execquery) method and passing a WQL query.

A synchronous query is a query that maintains control over the process of your application for the duration of the query. A synchronous query has the potential of locking up your application for large queries or for queries over a network. Alternatively, you can run an asynchronous query that returns control to the application while the query is run. For more information, see [How to Perform an Asynchronous Configuration Manager Query by Using Managed Code](how-to-perform-an-asynchronous-query-by-using-managed-code.md)

> [!NOTE]
>
> Lazy properties are not returned in synchronous queries. For more information, see [How to Read Lazy Properties by Using WMI](how-to-read-lazy-properties-by-using-wmi.md).

### To perform a synchronous query

1. Set up a connection to the SMS Provider. For more information, see [How to Connect to an SMS Provider in Configuration Manager by Using WMI](how-to-connect-to-an-sms-provider-in-configuration-manager-by-using-wmi.md).
2. Using the SWbemServices object that you obtain from step one, use the ExecQuery method to get a [SWbemObjectSet](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemobjectset) collection containing the query results.
3. Iterate through the SWbemObjectSet collection to access a [SWbemObject](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemobject) for each object returned by the query.

## Example

The following example performs a synchronous query of all packages in Configuration Manager.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](calling-code-snippets.md).

```vbs
Sub QueryPackages(connection)

    On Error Resume next

    Dim packages
    Dim package

    ' Run the query.
    Set packages = _
        connection.ExecQuery("Select * From SMS_Package")

    If Err.Number<>0 Then
        Wscript.Echo "Couldn't get Packages"
        Wscript.Quit
    End If

    For Each package In packages
        WScript.Echo  package.Name
    Next

    If packages.Count=0 Then
        Wscript.Echo "No packages found"
    End If

End Sub
```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) | A valid connection to the SMS Provider. |

## See Also

[Windows Management Instrumentation](https://learn.microsoft.com/en-us/windows/win32/wmisdk/wmi-start-page) [Objects overview](configuration-manager-objects-overview.md) [How to Call a Configuration Manager Object Class Method by Using WMI](how-to-call-a-configuration-manager-object-class-method-by-using-wmi.md) [How to Connect to an SMS Provider in Configuration Manager by Using WMI](how-to-connect-to-an-sms-provider-in-configuration-manager-by-using-wmi.md) [How to Create a Configuration Manager Object by Using WMI](how-to-create-a-configuration-manager-object-by-using-wmi.md) [How to Delete a Configuration Manager Object by Using WMI](how-to-delete-a-configuration-manager-object-by-using-wmi.md) [How to Modify a Configuration Manager Object by Using WMI](how-to-modify-a-configuration-manager-object-by-using-wmi.md) [How to Perform an Asynchronous Configuration Manager Query by Using WMI](how-to-perform-an-asynchronous-configuration-manager-query-by-using-wmi.md) [How to Read a Configuration Manager Object by Using WMI](how-to-read-a-configuration-manager-object-by-using-wmi.md) [How to Read Lazy Properties by Using WMI](how-to-read-lazy-properties-by-using-wmi.md) [Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md) [Configuration Manager Result Sets](result-sets.md) [Configuration Manager Special Queries](special-queries.md) [About queries](about-configuration-manager-queries.md)
