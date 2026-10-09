---
title: "SMS_ImageUpdateStatusView Server WMI Class"
description: The SMS_ImageUpdateStatusView WMI class represents software update information that is used by offline servicing image.
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

# SMS_ImageUpdateStatusView Server WMI Class

The `SMS_ImageUpdateStatusView` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents software update information that is used by offline servicing image.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ImageUpdateStatusView : SMS_BaseClass
{
    SInt32 ErrorCode;
    SInt32 ImageIndex;
    String ImagePackageID;
    String PackageDescription;
    String PackageName;
    SInt32 UpdateID;
};
```

## Methods

The `SMS_ImageUpdateStatusView` class does not define any methods.

## Properties

`ErrorCode` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

Error code for software update installation.

`ImageIndex` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key]

Index for offline servicing image.

`ImagePackageID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

ID for offline servicing image.

`PackageDescription` Data type: `String`

Access type: Read/Write

Qualifiers: none

Description for offline servicing image.

`PackageName` Data type: `String`

Access type: Read/Write

Qualifiers: none

Name for offline servicing image.

`UpdateID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key]

ID for software update.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
