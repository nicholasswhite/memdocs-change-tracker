---
title: "SMS_StateMigrationUserNames Server WMI Class"
description: An SMS Provider server class in Configuration Manager that represents a localized username during state migration.
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

# SMS_StateMigrationUserNames Server WMI Class

The `SMS_StateMigrationUserNames` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that represents a localized user name during state migration.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_StateMigrationUserNames
{
      UInt32 LocaleID;
      String UserName;
};
```

## Methods

The `SMS_StateMigrationUserNames` class doesn't define any methods.

## Properties

`LocaleID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

ID of the locale associated with the user name.

`UserName` Data type: `String`

Access type: Read/Write

Qualifiers: None

The localized user name. The default value is "".

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  Your application uses this class to create objects that are embedded by the [SMS_StateMigration Server WMI Class](sms_statemigration-server-wmi-class.md) and accessed using the `UserNames` property. For an example of the use of this class, see How to Create an Association Between Two Computers in Configuration Manager.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See also

[SMS_StateMigration server WMI class](sms_statemigration-server-wmi-class.md)
