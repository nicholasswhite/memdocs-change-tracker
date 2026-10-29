---
description: Learn how to update the Advertisement Status in Configuration Manager console using SoftDistProgramCompletedSuccessfullyEvent message.
title: SoftDistProgramCompletedSuccessfullyEvent
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

# SoftDistProgramCompletedSuccessfullyEvent

The `SoftDistProgramCompletedSuccessfullyEvent` message, in Configuration Manager, is sent when a program is completed successfully with an exit code (not MIFsuccess). It appears in the **Advertisement Status** in the Configuration Manager console.

This class is derived from the [SMS_SofwareDistribution_Event](sms_sofwaredistribution_event.md) class, and each base class property must be set.

## Properties

`AdvertisementId` Data type: `String`

Derived from `SMS_SoftwareDistribution_Event`.

`DummyString2` Data type: `String`

This property does not have to be set.

`DummyString2` Data type: `String`

This property does not have to be set.

`DummyString3` Data type: `String`

This property does not have to be set.

`DummyString6` Data type: `String`

This property does not have to be set.

`DummyString7` Data type: `String`

This property does not have to be set.

`DummyString8` Data type: `String`

This property does not have to be set.

`PackageName` Data type: `String`

Derived from `SMS_SoftwareDistribution_Event`.

`ProgramName` Data type: `String`

Derived from `SMS_SoftwareDistribution_Event`.

`UserContext` Data type: `String`

This property does not have to be set.
