---
title: "SMS_CIRelation_Flat Server WMI Class"
description: The SMS_CIRelation_Flat Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that provides a flat list of relationship information for directly or indirectly related configuration items.
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

# SMS_CIRelation_Flat Server WMI Class

The `SMS_CIRelation_Flat` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that provides a flat list of relationship information for directly or indirectly related configuration items.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CIRelation_Flat : SMS_BaseClass
{
    UInt32 FromCIID;
    Boolean IsVersionSpecific;
    UInt32 Level;
    UInt32 RelationType;
    UInt32 ToCIID;
};
```

## Methods

The `SMS_CIRelation_Flat` class does not define any methods.

## Properties

`FromCIID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

[SMS_CIRelation Server WMI Class](../sum/sms_cirelation-server-wmi-class.md)

`IsVersionSpecific` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

[SMS_CIRelation Server WMI Class](../sum/sms_cirelation-server-wmi-class.md)

`Level` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Level represents the depth of the relationships between configuration items. A direct relationship to the configuration item is 1 and an indirect relationship can be 2 or higher.

`RelationType` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

[SMS_CIRelation Server WMI Class](../sum/sms_cirelation-server-wmi-class.md)

`ToCIID` Data type: `UInt32`

Access type: Read/Write

Qualifiers: [key]

[SMS_CIRelation Server WMI Class](../sum/sms_cirelation-server-wmi-class.md)

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
