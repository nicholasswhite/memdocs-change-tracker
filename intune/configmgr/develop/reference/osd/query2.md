---
title: Query2
description: In Configuration Manager, Query2 specifies a query that is used to identify the platform that a client computer is running. This information should come from SMS_SupportedPlatforms Server WMI class objects and match the platform information specified in the PlatformApplicabilityCondition node.
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

# Query2

`Query2` specifies a query, in Configuration Manager, that is used to identify the platform that a client computer is running.

> [!NOTE]
>
> This information should come from `SMS_SupportedPlatforms Server WMI Class` objects and match the platform information specified in the PlatformApplicabilityCondition node.

The query is run on the client computer and typically inspects Windows Management Instrumentation (WMI) to determine the client platform. For example, `SELECT * FROM Win32_Processor WHERE Architecture=9 AND DataWidth=64`.

**Type**: Element.

**Instances**: One.

## Attributes

None

## See Also

[Operating System Deployment Driver Supported Platforms Schema](operating-system-deployment-driver-supported-platforms-schema.md) [PlatformApplicabilityCondition](platformapplicabilitycondition.md) [Query1](query1.md)
