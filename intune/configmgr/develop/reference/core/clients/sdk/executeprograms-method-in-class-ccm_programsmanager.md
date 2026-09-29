---
description: Learn how to manage downloads of legacy software distribution programs in Configuration Manager with ExecutePrograms class.
title: "ExecutePrograms Method in Class CCM_ProgramsManager"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ExecutePrograms Method in Class CCM_ProgramsManager

The `ExecutePrograms` WMI class method, in Configuration Manager, manages downloads of legacy software distribution programs.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 ExecutePrograms(
     [IN]  CCM_Program CCMPrograms[],
     [IN]  String SDKCallerId
);
```

#### Parameters

`CCMPrograms[]` Data type: `CCM_Program`

Qualifiers: [in]

Array of software distribution programs to download.

`SDKCallerId` Data type: `String`

Qualifiers: [in]

Identifier of the caller.

## Return Values

A `UInt32` data type that is 0 to indicate success or nonzero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[CCM_ProgramsManager Client WMI Class](ccm_programsmanager-client-wmi-class.md)
