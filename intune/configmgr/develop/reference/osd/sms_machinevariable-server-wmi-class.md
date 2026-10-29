---
title: "SMS_MachineVariable Server WMI Class"
description: The SMS_MachineVariable WMI class defines the settings of a task sequence variable that is unique to a specific computer.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_MachineVariable Server WMI Class

The `SMS_MachineVariable` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that defines the settings of a task sequence variable that is unique to a specific computer.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_MachineVariable
{
      Boolean IsMasked;
      String Name;
      String Value;
};
```

## Methods

The `SMS_MachineVariable` class doesn't define any methods.

## Properties

`IsMasked` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

This property isn't currently used.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The name of the machine variable. The default value is "".

`Value` Data type: `String`

Access type: Read/Write

Qualifiers: None

The machine variable value. The default value is `null`.

## Remarks

The task sequence variable can customize the behavior of a task sequence for a specific computer, and it overrides any definition that is set by [SMS_CollectionVariable Server WMI Class](sms_collectionvariable-server-wmi-class.md). These variables are automatically replicated down through the site hierarchy. For example, if a variable is declared on the primary child site server, it will be available on the primary grandchild site server, but not on the primary site server.

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers that are included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  Your application uses this class to create objects that are embedded by the [SMS_MachineSettings Server WMI Class](sms_machinesettings-server-wmi-class.md) and accessed by using the `MachineVariables` property. For an example of the use of this class, see How to Create a Computer Variable in Configuration Manager.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MachineSettings Server WMI Class](sms_machinesettings-server-wmi-class.md) [SMS_CollectionVariable Server WMI Class](sms_collectionvariable-server-wmi-class.md)
