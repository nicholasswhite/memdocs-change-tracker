---
description: Learn how to represent a collection variable that is accessible at the time of task execution using SMS_CollectionVariable.
title: "SMS_CollectionVariable Server WMI Class"
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

# SMS_CollectionVariable Server WMI Class

The `SMS_CollectionVariable` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a collection variable that is accessible at the time of task execution.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CollectionVariable
{
      Boolean IsMasked;
      String Name;
      String Value;
};
```

## Methods

The `SMS_CollectionVariable` class does not define any methods.

## Properties

`IsMasked` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

This value should be set to `true` if the collection variable contains a sensitive value such as a password. If the value is set to `true`, the SMS Provider treats this property as write-only and disallows reads. The default value is `false`.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Collection variable name. The default value is "".

`Value` Data type: `String`

Access type: Read/Write

Qualifiers: None

Collection variable value. The default value is "".

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  Collection variables are associated with collections as collection extended properties.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_CollectionSettings Server WMI Class](../core/clients/collections/sms_collectionsettings-server-wmi-class.md)
