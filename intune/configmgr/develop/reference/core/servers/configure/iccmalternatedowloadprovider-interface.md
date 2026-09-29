---
description: Learn how to use the ICcmAlternateDownloadProvider Interface to define the interface for an alternative download provider to be invoked by Content Transfer Manager to download packages.
title: ICcmAlternateDownloadProvider Interface
ms.date: "2017-07-25T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# ICcmAlternateDownloadProvider Interface

The **ICcmAlternateDownloadProvider** interface, in Configuration Manager, defines the interface for an alternative download provider to be invoked by Content Transfer Manager to download packages.

## Syntax

```
[
    uuid(89F7454D-71F7-4F05-8276-FADC8B85F48D),
    object,
    pointer_default(unique)
]

```

## Methods

The **ICcmAlternateDownloadProvider** interface defines the following methods.

| Method | Description |
| --- | --- |
| [ICcmAlternatedownloadProvider : CancelJob Method](iccmalternatedownloadprovider---canceljob-method.md) | Cancels a job. |
| [ICcmAlternatedownloadProvider : DownloadContent Method](iccmalternatedownloadprovider---downloadcontent-method.md) | Instructs the provider to download content. |
| [ICcmAlternatedownloadProvider : ModifyJobSource Method](iccmalternatedownloadprovider---modifyjobsource-method.md) | Instructs the provider to modify the source location for a given job. |
| [ICcmAlternatedownloadProvider : ModifyJobPriority Method](iccmalternatedownloadprovider---modifyjobpriority-method.md) | Instructs the provider to modify the priority for a given job. |
| [ICcmAlternatedownloadProvider : ModifyJobTimeout Method](iccmalternatedownloadprovider---modifyjobtimeout-method.md) | Instructs the provider to modify the timeout for a given job. |
| [ICcmAlternatedownloadProvider : Resume Method](iccmalternatedownloadprovider---resume-method.md) | Instructs the provider to resume a given job. |
| [ICcmAlternatedownloadProvider : Suspend Method](iccmalternatedownloadprovider---suspend-method.md) | Suspends a given job. |

## Remarks

ISVs should implement this interface and create an instance of local CCM_DownloadProvider policy that corresponds to their implementation.

> [!IMPORTANT]
>
> This interface must be implemented out-of-process from ccmexec.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
