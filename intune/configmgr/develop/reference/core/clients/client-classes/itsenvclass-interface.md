---
description: Learn how to represent the operating system deployment task sequencing environment with ITSEnvClass.
title: ITSEnvClass Interface
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43093068-2dda-408b-b3fe-dfd705c84f78
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/e453d60d-ba7e-43bc-8028-ec38e6b62512
---

# ITSEnvClass Interface

The `ITSEnvClass` automation interface, in Configuration Manager, represents the operating system deployment task sequencing environment. This interface inherits from `IDispatch`.

## In This Section

| Term | Definition |
| --- | --- |
| [ITSEnvClass::Clear](itsenvclass--clear-method.md) | Clears an operating system deployment task sequence environment. |
| [ITSEnvClass::Create](itsenvclass--create-method.md) | Creates an operating system deployment task sequence environment. |
| [ITSEnvClass::GetVariables](itsenvclass--getvariables-method.md) | Gets the variables for the operating system deployment task sequence environment. |
| [ITSEnvClass::Value](itsenvclass--value-property.md) | Contains the value of an operating system deployment task sequence environment variable. |

## Remarks

The UUID for `ITSEnvClass` is 063B1AB6-598F-49D9-9B6D-68163476355F.

## See Also

[Operating System Deployment Client COM Automation Classes](operating-system-deployment-client-com-automation-classes.md) [SMS_TaskSequence Server WMI Class](../../../osd/sms_tasksequence-server-wmi-class.md) [Task sequence overview](../../../../osd/operating-system-deployment-task-sequences-overview.md)
