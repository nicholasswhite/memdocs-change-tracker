---
description: Learn how to perform a synchronous query for Configuration Manager objects and implement a sink method to handle query results.
title: "How to Perform an Asynchronous Configuration Manager Query by Using WMI"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
---

# How to Perform an Asynchronous Configuration Manager Query by Using WMI

In Configuration Manager, you perform a synchronous query for Configuration Manager objects by calling the [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) object [ExecQueryAsync](https://learn.microsoft.com/en-us/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync) method and by implementing a sink method to handle query results.

To handle each returned object, create an [objWbemSink.OnObjectReady](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemsink-onobjectready) event subroutine. To be notified when the query is completed, create a [objWbemSink.OnCompleted](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemsink-oncompleted) event subroutine.

> [!NOTE]
>
> Lazy properties are not returned in asynchronous queries. For more information, see [How to Read Lazy Properties by Using WMI](how-to-read-lazy-properties-by-using-wmi.md).

### To perform an asynchronous query

1. Set up a connection to the SMS Provider. For more information, see [How to Connect to an SMS Provider in Configuration Manager by Using WMI](how-to-connect-to-an-sms-provider-in-configuration-manager-by-using-wmi.md).
2. Create an [OnObjectReady](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemsink-onobjectready) subroutine to handle objects by the query.
3. Create an [OnCompleted](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemsink-oncompleted) subroutine to handle query completion.
4. Using the [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) object you obtain from step one, use [ExecQueryAsync](https://learn.microsoft.com/en-us/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync) object to query Configuration Manager objects asynchronously.

## Example

The following VBScript code example asynchronously queries for all [SMS_Collection](../../reference/core/clients/collections/sms_collection-server-wmi-class.md) objects.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](calling-code-snippets.md).

```vbs
Dim bdone
Sub QueryCollection(connection)

    Dim sink
    bdone = False

    Set sink = WScript.CreateObject("wbemscripting.swbemsink","sink_")

    ' Query for all collections.
    connection.ExecQueryAsync sink, "select * from SMS_Collection"

    ' Wait until all instances are returned.
    While Not bdone
        wscript.sleep 1000
    Wend
 End Sub

' The sink subroutine to handle the OnObjectReady
' event. This is called as each object returns.
Sub sink_OnObjectReady(collection, octx)
    WScript.Echo "CollectionID: " + collection.CollectionID
    WScript.Echo "Name: " + collection.Name
    Wscript.Echo
End Sub

' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned.
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
Sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "All collections returned"
    bdone = true
End Sub
```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) | A valid connection to the SMS Provider. |

## See Also

[Windows Management Instrumentation](https://learn.microsoft.com/en-us/windows/win32/wmisdk/wmi-start-page) [Objects overview](configuration-manager-objects-overview.md) [How to Call a Configuration Manager Object Class Method by Using WMI](how-to-call-a-configuration-manager-object-class-method-by-using-wmi.md) [How to Connect to an SMS Provider in Configuration Manager by Using WMI](how-to-connect-to-an-sms-provider-in-configuration-manager-by-using-wmi.md) [How to Create a Configuration Manager Object by Using WMI](how-to-create-a-configuration-manager-object-by-using-wmi.md) [How to Delete a Configuration Manager Object by Using WMI](how-to-delete-a-configuration-manager-object-by-using-wmi.md) [How to Modify a Configuration Manager Object by Using WMI](how-to-modify-a-configuration-manager-object-by-using-wmi.md) [How to Perform a Synchronous Configuration Manager Query by Using WMI](how-to-perform-a-synchronous-configuration-manager-query-by-using-wmi.md) [How to Read a Configuration Manager Object by Using WMI](how-to-read-a-configuration-manager-object-by-using-wmi.md) [How to Read Lazy Properties by Using WMI](how-to-read-lazy-properties-by-using-wmi.md) [Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md) [Configuration Manager Result Sets](result-sets.md) [Configuration Manager Special Queries](special-queries.md) [About queries](about-configuration-manager-queries.md)
