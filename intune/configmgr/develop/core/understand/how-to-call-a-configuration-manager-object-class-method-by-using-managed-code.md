---
title: "How to Call a Configuration Manager Object Class Method by Using Managed Code"
description: To call a SMS Provider class method in Configuration Manager, use the ExecuteMethod method.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
---

# How to Call a Configuration Manager Object Class Method by Using Managed Code

To call a SMS Provider class method, in Configuration Manager, you use the [ExecuteMethod](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146186(v=msdn.10)) method. You populate a [Dictionary](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-6.0/aa239680(v=vs.60)) object with the method's parameters, and the return value is an [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) object that contains the result of the method call.

> [!NOTE]
>
> To call a method on an object instance, use the [ExecuteMethod](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146233(v=msdn.10)) method on the [IResultObject](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc147376(v=msdn.10)) object instance.

### To call a Configuration Manager object class method

1. Set up a connection to the SMS Provider. For more information, see [SMS Provider fundamentals](sms-provider-fundamentals.md).
2. Create the input parameters as a **Dictionary** object.
3. Using the **WqlConnectionManager** object instance, call [ExecuteMethod](https://learn.microsoft.com/en-us/previous-versions/system-center/developer/cc146186(v=msdn.10)) and specify the class name and input parameters.
4. Retrieve the method return value from the *ReturnValue* property in the returned **IResultObject** object.

## Example

The following example validates a collection rule query by calling the [SMS_CollectionRuleQuery](../../reference/core/clients/collections/sms_collectionrulequery-server-wmi-class.md) class [ValidateQuery](../../reference/core/clients/collections/validatequery-method-in-class-sms_collectionrulequery.md) class method.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](calling-code-snippets.md).

```
public void ValidateQueryRule(WqlConnectionManager connection, string wqlQuery)
{
    try
    {
        Dictionary<string,object> validateQueryParameters = new Dictionary<string,object>();

        // Add the sql query as the WQLQuery parameter.
        validateQueryParameters.Add("WQLQuery",wqlQuery);

        // Call the method
        IResultObject result=connection.ExecuteMethod("SMS_CollectionRuleQuery", "ValidateQuery", validateQueryParameters);

        if (result["ReturnValue"].BooleanValue == true)
        {
            Console.WriteLine (wqlQuery + " is a valid query");
        }
        else
        {
            Console.WriteLine (wqlQuery + " is not a valid query");
        }
     }
     catch (SmsException ex)
     {
           Console.WriteLine("Failed to validate query rule: ",ex.Message);
           throw;
     }
}

```

This example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | - Managed: **WqlConnectionManager** | A valid connection to the SMS Provider. |
| `wqlQuery` | - Managed: **IResultObject** | A WQL query string. For this example, `SELECT * FROM SMS_R_System` is a valid query. |

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

[Objects overview](configuration-manager-objects-overview.md) [How to Connect to a Configuration Manager Provider using Managed Code](how-to-connect-to-an-sms-provider-by-using-managed-code.md) [How to Create a Configuration Manager Object by Using Managed Code](how-to-create-a-configuration-manager-object-by-using-managed-code.md) [How to Modify a Configuration Manager Object by Using Managed Code](how-to-modify-a-configuration-manager-object-by-using-managed-code.md) [How to Perform an Asynchronous Configuration Manager Query by Using Managed Code](how-to-perform-an-asynchronous-query-by-using-managed-code.md) [How to Perform a Synchronous Configuration Manager Query by Using Managed Code](how-to-perform-a-synchronous-configuration-manager-query-by-using-managed-code.md) [How to Read a Configuration Manager Object by Using Managed Code](how-to-read-a-configuration-manager-object-by-using-managed-code.md)
