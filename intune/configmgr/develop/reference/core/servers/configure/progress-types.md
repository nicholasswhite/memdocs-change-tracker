---
title: Progress Types
description: Progress states for a download. For a non-status change (for example, if there was just transfer of bytes), specify NULL for progress type.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Progress Types

Progress states for a download.

> [!NOTE]
>
> For a non-status change (for example, if there was just transfer of bytes), specify NULL for progress type.

## Syntax

```
//  Progress types:
//******************************************************************************
static const WCHAR S_DTS_PROGRESS_DOWNLOADING_MANIFEST[]    = L"DownloadingManifest";
static const WCHAR S_DTS_PROGRESS_PROCESSING_MANIFEST[]     = L"ProcessingManifest";
static const WCHAR S_DTS_PROGRESS_CREATING_DIRECTORIES[]    = L"CreatingDirectories";
static const WCHAR S_DTS_PROGRESS_PREPARING_DOWNLOAD[]      = L"PreparingDownload";
static const WCHAR S_DTS_PROGRESS_DOWNLOADING_DATA[]        = L"DownloadingData";

```

## Types

| Progress type | Description |
| --- | --- |
| S_DTS_PROGRESS_DOWNLOADING_MANIFEST | Determining list of files to download. |
| S_DTS_PROGRESS_PROCESSING_MANIFEST | Processing list of files. |
| S_DTS_PROGRESS_CREATING_DIRECTORIES | Creating subdirectories based on list of files. |
| S_DTS_PROGRESS_PREPARING_DOWNLOAD | Manifest processing complete, starting download. |
| S_DTS_PROGRESS_DOWNLOADING_DATA | Downloading files. |

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
