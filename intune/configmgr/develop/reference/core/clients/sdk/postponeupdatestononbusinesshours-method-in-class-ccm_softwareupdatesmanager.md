---
description: Learn how to postpone a set of software updates to automatically install in specified non-business hours.
title: "PostponeUpdatesToNonBusinessHours Method in Class CCM_SoftwareUpdatesManager"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# PostponeUpdatesToNonBusinessHours Method in Class CCM_SoftwareUpdatesManager

The `PostoneUpdatesToNonBusinessHours` WMI class method, in Configuration Manager, postpones a set of software updates to automatically install in non-business hours, which are specified by the user.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 PostponeUpdatesToNonBusinessHours(
     [IN]  CCM_SoftwareUpdate CCMUpdates[],
     [IN]  Boolean RebootImmediatelyAfterInstall
);
```

#### Parameters

`CCMUpdates[]` Data type: `CCM_SoftwareUpdate`

Qualifiers: [in]

Array of software updates to be installed.

`RebootImmediatelyAfterInstall` Data type: `Boolean`

Qualifiers: [in]

`true` if the computer restarts immediately after the installation; otherwise, `false`.

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

[CCM_SoftwareUpdatesManager Client WMI Class](ccm_softwareupdatesmanager-client-wmi-class.md)
