---
title: "AllowThreat Method in Class SMS_ClientOperation"
description: In Configuration Manager, the AllowThreat WMI class method that allows the specified threat to all members in a specific collection.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# AllowThreat Method in Class SMS_ClientOperation

The `AllowThreat` Windows Management Instrumentation (WMI) class method in Configuration Manager that allows the specified threat (identified by `ThreatID`) to all members in a specific collection.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 AllowThreat
{
    [IN]    UInt64 ThreatID
    [IN]    String AllowSettingsUniqueID
    [IN]    String TargetCollectionID
    [OUT]   UInt32 OperationID
};
```

## Parameters

`ThreatID` Data type: `UInt64`

Qualifiers: [id("0"), in]

Threat identifier.

`AllowSettingsUniqueID` Data type: `String`

Qualifiers: [id("1"), in]

Antimalware settings (with allow threat identifier enabled) unique identifier.

`TargetCollectionID` Data type: `String`

Qualifiers: [id("2"), in]

Identifier of target collection.

`OperationID` Data type: `UInt32`

Qualifiers: [id("3"), out]

Unique identifier for the operation.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_ClientOperation Server WMI Class](sms_clientoperation-server-wmi-class.md)
