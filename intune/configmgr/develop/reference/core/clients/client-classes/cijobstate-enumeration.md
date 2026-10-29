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
