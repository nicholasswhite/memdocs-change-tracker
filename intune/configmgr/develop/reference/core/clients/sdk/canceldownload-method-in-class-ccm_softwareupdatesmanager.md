---
description: Learn how to cancel an in-progress download of software updates during a deployment using the CancelDownload class method.
title: "CancelDownload Method in Class CCM_SoftwareUpdatesManager"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# CancelDownload Method in Class CCM_SoftwareUpdatesManager

The `CancelDownload` WMI class method, in Configuration Manager, cancels an in-progress download of software updates during a deployment.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
UInt32 CancelDownload();
```

#### Parameters

None.

## Return Values

A `UInt32` data type that is 0 to indicate success or nonzero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Remarks

The `CancelDownload` method cancels the download only for deployments that are initiated by the Software Updates Client Agent or through the Configuration Manager SDK. If the software updates deployment was initiated as the result of a deadline, the call to this method fails.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[CCM_SoftwareUpdatesManager Client WMI Class](ccm_softwareupdatesmanager-client-wmi-class.md)
