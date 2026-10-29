---
title: "SMS_UserVariable Server WMI Class"
description: The SMS_UserVariable Windows Management Instrumentation (WMI) class defines the settings of a specific user.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_UserVariable Server WMI Class

The `SMS_UserVariable` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that defines the settings of a specific user (such as IsCloudUser=True/False).

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_UserVariable
{
      Boolean IsMasked;
      String Name;
      String Value;
};
```

## Methods

The `SMS_UserVariable` class doesn't define any methods.

## Properties

`IsMasked` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

This property isn't currently used.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

The name of the user variable. The default value is "".

`Value` Data type: `String`

Access type: Read/Write

Qualifiers: None

The user variable value. The default value is `null`.

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers that are included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  Your application uses this class to create objects that are embedded by the SMS_UserSettings Server WMI Class and accessed by using the `UserVariables` property.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_CollectionVariable Server WMI Class](sms_collectionvariable-server-wmi-class.md)
