---
description: Learn how the following example shows how to configure the properties of an existing package, in Configuration Manager, by using the SMS_Package class.
title: "How to Configure Package Properties"
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

# How to Configure Package Properties

The following example shows how to configure the properties of an existing package, in Configuration Manager, by using the `SMS_Package` class.

### To configure an existing package

1. Set up a connection to the SMS Provider.
2. Load the existing package object by using `SMS_Package` class.
3. Populate any package properties (this example uses package description).
4. Save the package and the new package properties.

## Example

The following example method configures package properties for software distribution.

For information about calling the sample code, see [Calling Configuration Manager Code Snippets](../../understand/calling-code-snippets.md).

```vbs

Sub ConfigurePackageProperties(connection, existingPackageID, newPackageDescription)

    ' Get the specific package object.     Dim packageToConfigure
    Set packageToConfigure = connection.Get("SMS_Package.PackageID='" & existingPackageID & "'")

    ' Replace the existing package property (in this case the package description).
    packageToConfigure.Description = newPackageDescription

    ' Save the package with the modified properties.
    packageToConfigure.Put_

    ' Output package ID and package name.
    wscript.echo "Configured Package "
    wscript.echo "Package ID:        "  & packageToConfigure.PackageID
    wscript.echo "Package Name:      "  & packageToConfigure.Name

End Sub

```

```c#

public void ConfigurePackageProperties(WqlConnectionManager connection, string existingPackageID, string newPackageDescription)
{
    try
    {
        // Get specific package instance to modify.
        IResultObject packageToConfigure = connection.GetInstance(@"SMS_Package.PackageID='" + existingPackageID + "'");

        // Replace the existing package property with the new value (in this case the package description).
        packageToConfigure["Description"].StringValue = newPackageDescription;

        // Save package and modified package properties.
        packageToConfigure.Put();

        // Output package ID and package name.
        Console.WriteLine("Configured Package ");
        Console.WriteLine("Package ID:        " + packageToConfigure["PackageID"].StringValue);
        Console.WriteLine("Package Name:      " + packageToConfigure["Name"].StringValue);
    }

    catch (SmsException ex)
    {
        Console.WriteLine("Failed to configure package. Error: " + ex.Message);
        throw;
    }
}

```

The example method has the following parameters:

| Parameter | Type | Description |
| --- | --- | --- |
| `connection`   `swbemServices` | - Managed: `WqlConnectionManager` - VBScript: [SWbemServices](https://learn.microsoft.com/en-us/windows/win32/wmisdk/swbemservices) | A valid connection to the SMS Provider. |
| `existingPackageID` | - Managed: `String` - VBScript: `String` | The ID of the existing package. |
| `newPackageDescription` | - Managed: `String` - VBScript: `String` | The description for the new package. |

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

[Software distribution overview](software-distribution-overview.md) [SMS_SCI_Component Server WMI Class](../../../reference/core/servers/configure/sms_sci_component-server-wmi-class.md)
