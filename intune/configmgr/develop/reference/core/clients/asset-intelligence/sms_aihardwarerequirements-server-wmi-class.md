---
description: Learn how to associate a software title with hardware requirements using SMS_AIHardwareRequirements in Configuration Manager.
title: "SMS_AIHardwareRequirements Server WMI Class"
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

# SMS_AIHardwareRequirements Server WMI Class

The `SMS_AIHardwareRequirements` Windows Management Instrumentation (WMI) class, in Configuration Manager, associates a software title with hardware requirements.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AIHardwareRequirements : SMS_BaseClass
{
      boolean IsLocal;
      uint32 MinCPU;
      sint64 MinDiskFree;
      sint64 MinDiskSize;
      sint64 MinRAM;
      string Product;
      uint32 State;
};
```

## Methods

The following table lists the methods in the `SMS_AIHardwareRequirements` class.

| Method | Description |
| --- | --- |
| [GetSummary Method in Class SMS_AIHardwareRequirements](getsummary-method-in-class-sms_aihardwarerequirements.md) | Retrieves a summary of all class instances based on the State property of the class. |

## Properties

`IsLocal` Data type: `Boolean`

Access type: Read Only

Qualifiers: None

`true` when this entry has been created locally. Local entries are editable.

`MinCPU` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Minimum CPU in megahertz.

`MinDiskFree` Data type: `SInt64`

Access type: Read/Write

Qualifiers: None

Minimum free disk space in KB.

`MinDiskSize` Data type: `SInt64`

Access type: Read/Write

Qualifiers: None

Minimum total disk size in KB.

`MinRAM` Data type: `SInt64`

Access type: Read/Write

Qualifiers: None

Minimum total RAM in KB.

`Product` Data type: `String`

Access type: Read/Write

Qualifiers: key

The software title.

`State` Data type: `UInt32`

Access type: Read Only

Qualifiers: None

| Value | Description |
| --- | --- |
| 0 | Validated, defined by Microsoft through System Center Online. |
| 1 | User-defined. |

## Remarks

Class qualifiers for this class include:

- DisplayName("AI Hardware Requirements")
- Dynamic
- Provider("ExtnProv")
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Initiate Asset Intelligence synchronization](../../../../core/clients/asset-intelligence/how-to-initiate-a-synchronization.md)
