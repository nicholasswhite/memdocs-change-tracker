---
title: "Configuration Manager Embedded Objects"
description: You cannot use Windows Management Instrumentation (WMI) to enumerate, query, get, or put embedded objects. You can only retrieve and store embedded objects through the parent instance.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
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

# Configuration Manager Embedded Objects

Configuration Manager embedded objects do not exist by themselves in the Common Information Model (CIM) repository — they exist within other objects. As a result, you cannot use Windows Management Instrumentation (WMI) to enumerate, query, get, or put embedded objects. You can only retrieve and store embedded objects through the parent instance.

Embedded objects are commonly used when accessing the site control file. In this case, special embedded objects, such as properties and property lists are used.

When a class or method contains an embedded object of an abstract type, such as `SMS_ScheduleToken`, you store and retrieve classes that are inherited from it. For example, instead of using `SMS_ScheduleToken`, you use one of the embedded objects inherited from it, such as `SMS_ST_RecurWeekly`.

## See Also

[How to Read and Write to the Configuration Manager Site Control File by Using Managed Code](how-to-read-and-write-to-the-site-control-file-by-using-managed-code.md) [How to Read and Write to the Configuration Manager Site Control File by Using WMI](how-to-read-and-write-to-the-site-control-file-by-using-wmi.md)
