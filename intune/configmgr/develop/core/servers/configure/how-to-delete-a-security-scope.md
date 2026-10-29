---
title: "How to Delete a Security Scope"
description: Learn how to delete a security scope in Configuration Manager by using the SMS_SecuredCategory class.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# How to Delete a Security Scope

The following example shows how to delete a security scope in Configuration Manager by using the `SMS_SecuredCategory` class.

### To delete a security scope

1. Set up a connection to the SMS Provider.
2. Load the existing security scope by using the `SMS_SecuredCategory` WMI class
3. Delete the security scope by using the delete method.

## Example

The following example deletes a security scope by identifier:

```vbs
Sub DeleteSecurityScope(connection, scopeId)
    Dim scope
    ' Get the existing scope by identifier.
    Set scope = connection.Get("SMS_SecuredCategory.CategoryID='" & scopeId & "'")

    ' Make sure we are allowed to delete this scope.
    If (scope.IsBuiltIn) Then
        Err.Raise 1, "DeleteSecurityScope", "Deleting a built-in security scope is not allowed."
    Else
        scope.Delete_
    End If
End Sub
```

```c#
public void DeleteSecurityScope(WqlConnectionManager connection, string scopeId)
{
    // Get the existing scope by identifier.
    IResultObject secScope = connection.GetInstance("SMS_SecuredCategory.CategoryID='" + scopeId + "'");

    // Make sure we are allowed to delete this scope.
    if (secScope.Properties["IsBuiltIn"].BooleanValue == true)
        throw new System.Exception("Deleting a built-in security scope is not allowed.");
    else
        secScope.Delete();
}
```

The example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection` | - Managed: `WqlConnectionManager` - VBScript: [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) | A valid connection to the SMS Provider. |
| `scopeId` | `String` | The identifier of the security scope to delete. |

## Compiling the Code

The C# example requires:

### Namespaces

Microsoft.ConfigurationManagement.ManagementProvider

Microsoft.ConfigurationManagement.ManagementProvider.WqlQueryEngine

### Assembly

adminui.wqlqueryengine

microsoft.configurationmanagement.managementprovider

## Robust Programming

For more information about error handling, see [About Configuration Manager Errors](../../understand/about-configuration-manager-errors.md).

## See Also

[How to Create a New Security Scope](how-to-create-a-new-security-scope.md) [How to Associate an Object with a Security Scope](how-to-associate-an-object-with-a-security-scope.md) [How to Remove an Object Association with a Security Scope](how-to-remove-an-object-association-with-a-security-scope.md) [SMS_SecuredCategory Server WMI Class](../../../reference/core/servers/configure/sms_securedcategory-server-wmi-class.md)
