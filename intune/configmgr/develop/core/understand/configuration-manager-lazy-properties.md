---
title: "Configuration Manager Lazy Properties"
description: If lazy properties are retrieved during query operations, they have null or zero values.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: article
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
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Configuration Manager Lazy Properties

Some Configuration Manager object properties are relatively inefficient to retrieve. If these properties were retrieved for many instances in a class (as might be done in a query), the response would be considerably delayed. Such properties are considered lazy properties and are not usually retrieved during query operations. However, if these properties are retrieved during a query, they have `null` or zero values, which might not be the actual value of the property for every instance. Therefore, if you want to get the correct value for lazy properties, you must get each instance individually.

## See Also

[How to Read Lazy Properties Using Managed Code](how-to-read-lazy-properties-by-using-managed-code.md) [How to Read Lazy Properties Using WMI](how-to-read-lazy-properties-by-using-wmi.md)
