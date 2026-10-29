---
title: "SMS_ImageDiskInformation Server WMI Class"
description: The SMS_ImageDiskInformation WMI class is an SMS Provider server class, in Configuration Manager, that represents all disks and partition information in an operating system image and installer.
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

# SMS_ImageDiskInformation Server WMI Class

The `SMS_ImageDiskInformation` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents all disks and partition information in an operating system image and operating system installer.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ImageDiskInformation : SMS_BaseClass
{
    UInt32 DiskIndex;
    String DiskStyle;
    String PackageID;
    String PartitionFileSystem;
    UInt32 PartitionIndex;
    Boolean PartitionIsBoot;
    String PartitionLabel;
    SInt64 PartitionOffset;
    SInt64 PartitionSize;
    String PartitionStyle;
    String PartitionType;
};
```

## Methods

The `SMS_ImageDiskInformation` class does not define any methods.

## Properties

`DiskIndex` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Disk Index of this image.

`DiskStyle` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Disk style.

`PackageID` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

ID of the image package.

`PartitionFileSystem` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Partition file system.

`PartitionIndex` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Partition index of this image.

`PartitionIsBoot` Data type: `Boolean`

Access type: Read-only

Qualifiers: [read]

Whether the partition is the boot partition.

`PartitionLabel` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Partition label.

`PartitionOffset` Data type: `SInt64`

Access type: Read-only

Qualifiers: [read]

Partition offset.

`PartitionSize` Data type: `SInt64`

Access type: Read-only

Qualifiers: [read]

Partition size.

`PartitionStyle` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Partition style.

`PartitionType` Data type: `String`

Access type: Read-only

Qualifiers: [read]

Partition type.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
