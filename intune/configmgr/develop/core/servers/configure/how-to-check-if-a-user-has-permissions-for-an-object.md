---
title: "How to Check if a User Has Permissions for an Object"
description: In Configuration Manager, you can check for object permissions using the UserHasPermissions Method in Class SMS_RbacSecuredObject.
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

# How to Check if a User Has Permissions for an Object

In Configuration Manager, you can check for object permissions using the [UserHasPermissions Method in Class SMS_RbacSecuredObject](../../../reference/core/servers/configure/userhaspermissions-method-in-class-sms_rbacsecuredobject.md).

### To check if a user has permissions for an object

1. Create a dictionary object to pass object name and permissions to check for to the [UserHasPermissions Method in Class SMS_RbacSecuredObject](../../../reference/core/servers/configure/userhaspermissions-method-in-class-sms_rbacsecuredobject.md).
2. Call the [UserHasPermissions Method in Class SMS_RbacSecuredObject](../../../reference/core/servers/configure/userhaspermissions-method-in-class-sms_rbacsecuredobject.md), passing in the dictionary object.
3. The method returns `true`, if the user has the permissions.

## Example

The following example checks to see if the user has the indicated permissions:

```c#
public static bool UserHasPermissions(ConnectionManagerBase connectionManager, string objectName, int permissions, out int currentPermissions)
{
    if (connectionManager == null)
    {
        throw new ArgumentNullException("connectionManager");
    }
    if (string.IsNullOrEmpty(objectName) == true)
    {
        throw new ArgumentException("The parameter 'objectName' cannot be null or an empty string", "objectName");
    }
    IResultObject outParams = null;
    try
    {
        Dictionary<string, object> inParams = new Dictionary<string, object>();
        inParams["ObjectPath"] = objectName;
        inParams["Permissions"] = permissions;
        outParams = connectionManager.ExecuteMethod("SMS_RbacSecuredObject", "UserHasPermissions", inParams);
       if (outParams != null)
       {
            currentPermissions = outParams["Permissions"].IntegerValue;
            return outParams["ReturnValue"].BooleanValue;
       }
    }
    finally
    {
        if (outParams != null)
        {
            outParams.Dispose();
        }
    }
    currentPermissions = 0;
    return false;
}

```

The example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connectionManager` | - Managed: `connectionManager` | A valid connection to the SMS Provider. |
| `objectName` | `String` | Name of the object. |
| permissions | Integer | The permissions. |
| currentPermissions | Integer | The current permissions. |

## Compiling the Code

The C# example requires:

### Namespaces

Microsoft.ConfigurationManagement.ManagementProvider

Microsoft.ConfigurationManagement.ManagementProvider.WqlQueryEngine

System

### Assembly

adminui.wqlqueryengine

microsoft.configurationmanagement.managementprovider

mscorlib

## Robust Programming

For more information about error handling, see [About Configuration Manager Errors](../../understand/about-configuration-manager-errors.md).

## See Also

[SMS_Admin Server WMI Class](../../../reference/core/servers/configure/sms_admin-server-wmi-class.md) [SMS_Role Server WMI Class](../../../reference/core/servers/configure/sms_role-server-wmi-class.md) [SMS_SecuredCategory Server WMI Class](../../../reference/core/servers/configure/sms_securedcategory-server-wmi-class.md)
