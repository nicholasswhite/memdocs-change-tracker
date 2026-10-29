---
title: "Sample queries for client status in Configuration Manager"
description: Sample queries that show how to join common client status views to other views.
ms.date: "2019-04-30T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to


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

# Sample queries for client status in Configuration Manager

The following sample queries demonstrate how to join common client status views to other views.

## Joining client status and collection views

This query lists each client computer in the site, the last time it requested policy, and the collections to which the computer belongs. The query uses the **v_CH_PolicyRequestHistory** view to read the last policy request time and joins, using the **ResourceID** column to the **v_ClientCollectionMembers** view.

```sql
    SELECT        dbo.CH_PolicyRequestHistory.MachineID AS ResourceID, dbo.CH_PolicyRequestHistory.RequestTime, dbo.v_ClientCollectionMembers.CollectionID
    FROM            dbo.CH_PolicyRequestHistory INNER JOIN
                             dbo.v_ClientCollectionMembers ON dbo.CH_PolicyRequestHistory.MachineID = dbo.v_ClientCollectionMembers.ResourceID
```

## See also

[Client status views in Configuration Manager](client-status-views-configuration-manager.md)
