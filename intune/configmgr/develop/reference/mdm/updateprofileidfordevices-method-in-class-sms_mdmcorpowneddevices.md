---
title: "UpdateProfileIDForDevices Method in Class SMS_MDMCorpOwnedDevices"
description: Update the profile IDs for device serial numbers.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# UpdateProfileIDForDevices Method in Class SMS_MDMCorpOwnedDevices

The `UpdateProfileIdForDevices` Windows Management Instrumentation (WMI) class method, in Configuration Manager, updates the profile IDs for device serial numbers.

## Syntax

```
sint32 UpdateProfileIdForDevices(
     String RequestEnrollmentProfileId,
     String DeviceSerialNumbers
);

```

#### Parameters

`RequestEnrollmentProfileId` Data type: `String`

Qualifiers: [in]

Enrollment profile ID.

`DeviceSerialNumbers` Data type: `String Array`

Qualifiers: [in]

The serial number of the device.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MDMCorpOwnedDevices Server WMI Class](sms_mdmcorpowneddevices-server-wmi-class.md)
