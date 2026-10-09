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
