---
description: Learn how the SMS_FailedImageUpdateView Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that represents failed software update information in offline servicing image.
title: "SMS_FailedImageUpdateView Server WMI Class"
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

# SMS_FailedImageUpdateView Server WMI Class

The `SMS_FailedImageUpdateView` Windows Management Instrumentation (WMI) class is an SMS Provider server class in Configuration Manager that represents failed software update information in offline servicing image.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_FailedImageUpdateView : SMS_BaseClass
{
    SInt32 FailedImageCount;
    String Title;
    SInt32 UpdateID;
};
```

## Methods

The `SMS_FailedImageUpdateView` class doesn't define any methods.

## Properties

`FailedImageCount` Data type: `SInt32`

Access type: Read/Write

Qualifiers: none

Offline image count that failed to install this update.

`Title` Data type: `String`

Access type: Read/Write

Qualifiers: none

Software update display name.

`UpdateID` Data type: `SInt32`

Access type: Read/Write

Qualifiers: [key]

Software update local unique ID.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
