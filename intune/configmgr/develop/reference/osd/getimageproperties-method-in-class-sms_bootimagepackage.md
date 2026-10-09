---
title: "GetImageProperties Method in Class SMS_BootImagePackage"
description: The GetImageProperties WMI class method reads all metadata from the specified .wim source file for a boot image to an XML string.
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

# GetImageProperties Method in Class SMS_BootImagePackage

The `GetImageProperties` Windows Management Instrumentation (WMI) class method, in Configuration Manager, reads all metadata from the specified .wim source file for a boot image to an XML string.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 GetImageProperties(
      String SourceImagePath,
      String ImageProperty
);
```

#### Parameters

`SourceImagePath` Data type: `String`

Qualifiers: [in]

Path to the .wim source file to query for metadata.

`ImageProperty` Data type: `String`

Qualifiers: [out]

XML document containing the image metadata.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Remarks

This method accesses the source .wim file metadata by using the `ImageProperty` property of [SMS_BootImagePackage Server WMI Class](sms_bootimagepackage-server-wmi-class.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_BootImagePackage Server WMI Class](sms_bootimagepackage-server-wmi-class.md) [ReloadImageProperties Method in Class SMS_BootImagePackage](reloadimageproperties-method-in-class-sms_bootimagepackage.md)
