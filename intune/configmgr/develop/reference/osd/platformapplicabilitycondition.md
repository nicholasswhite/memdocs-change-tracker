---
description: Learn how to specify one supported platform for an operating system deployment driver in Configuration Manager using PlatformApplicabilityCondition.
title: PlatformApplicabilityCondition
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

# PlatformApplicabilityCondition

`PlatformApplicabilityCondition` specifies one supported platform for an operating system deployment driver in Configuration Manager.

> [!NOTE]
>
> It is only valid to populate this information with values from `SMS_SupportedPlatforms Server WMI Class` objects. Drivers can be targeted only at major releases, for example, all Windows.

**Type**: String.

**Instances**: Zero or more.

## Attributes

| Attribute | Description |
| --- | --- |
| DisplayName | The platform name displayed in the Configuration Manager console. |
| MaxVersion | The maximum supported version. For example, "5.20.9999.9999". |
| MinVersion | The minimum supported version. For example, "5.20.3790.0". |
| Name | The operating system name. For example, "Windows NT". |
| Platform | The supported platform, for example, "x64". |

## See Also

[Operating System Deployment Driver Supported Platforms Schema](operating-system-deployment-driver-supported-platforms-schema.md) [PlatformApplicabilityConditions](platformapplicabilityconditions.md) [Query1](query1.md) [Query2](query2.md)
