---
title: "GetNextServiceWindowID Method in Class CCM_ServiceWindowManager"
description: In Configuration Manager, the GetNextServiceWindowID WMI class method gets the identifier of the next service window instance closest to the current time.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
---

# GetNextServiceWindowID Method in Class CCM_ServiceWindowManager

The `GetNextServiceWindowID` WMI class method, in Configuration Manager, gets the identifier of the next service window instance closest to the current time.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
uint32 GetNextServiceWindowID(
     [OUT] String NextServiceWindowID
);
```

#### Parameters

`NextServiceWindowID` Data type: `String`

Qualifiers: [out]

Identifier of the next service window instance closest to the current time.

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

[CCM_ServicewindowManager Client WMI Class](ccm_servicewindowmanager-client-wmi-class.md)
