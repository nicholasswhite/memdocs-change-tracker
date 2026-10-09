---
description: Learn how CIJobState enumeration defines configuration item agent job states and is used by ICIINFO Interface.
title: CIJobState Enumeration
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

# CIJobState Enumeration

In Configuration Manager, the `CIJobState` enumeration defines configuration item agent job states. This enumeration is used by the [ICIINFO Interface](iciinfo-interface.md).

## Syntax

```
typedef enum tagCIJobState
{
  ciJobStateNone = 0,
  ciJobStateAvailable,
  ciJobStateSubmitted,
  ciJobStateDetecting,
  ciJobStateDownloadingCIDef,
  ciJobStateDownloadingSdmPkg,
  ciJobStatePreDownload,
  ciJobStateDownloading,
  ciJobStateWaitInstall,
  ciJobStateInstalling,
  ciJobStatePendingSoftReboot,
  ciJobStatePendingHardReboot,
  ciJobStateWaitReboot,
  ciJobStateVerifying,
  ciJobStateInstallComplete,
  ciJobStateError,
  ciJobStateWaitServiceWindow
} CIJobState;
```

## Elements

`ciJobStateNone` No state.

`ciJobStateAvailable` Available.

`ciJobStateSubmitted` Submitted.

`ciJobStateDetecting` Being detected.

`ciJobStateDownloadingCIDef` Downloading configuration item definition.

`ciJobStateDownloadingSdmPkg` Downloading a System Definition Model (SDM) package.

`ciJobStatePreDownload` Pre-download.

`ciJobStateDownloading` Downloading.

`ciJobStateWaitInstall` Wait for installation.

`ciJobStateInstalling` Installing.

`ciJobStatePendingSoftReboot` Suspend operation for soft reboot.

`ciJobStatePendingHardReboot` Suspend operation for hard reboot.

`ciJobStateWaitReboot` Wait for reboot.

`ciJobStateVerifying` Verifying.

`ciJobStateInstallComplete` Installation complete.

`ciJobStateError` Error.

`ciJobStateWaitServiceWindow` Wait for maintenance window.

## See Also

[ICIINFO Interface](iciinfo-interface.md)
