---
title: "Sample queries for application management in Configuration Manager"
description: Sample queries that show how to join the most common application management views to other views.
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

# Sample queries for application management in Configuration Manager

The following sample queries demonstrate how to join the most common application management views to other views.

## Joining package and program deployment and collection views

The following query lists all package and program deployments by advertisement ID, advertisement name, and the collection that was targeted for the deployment. The **v_Advertisement** view is joined to the **v_Collection** view by using the **AdvertisementID** column.

```sql
    SELECT ADV.AdvertisementID, ADV.AdvertisementName, 
    COL.CollectionID, COL.Name as CollectionName 
    FROM v_Advertisement ADV INNER JOIN v_Collection COL 
    ON ADV.CollectionID = COL.CollectionID 
    ORDER BY ADV.AdvertisementID 
```

## See also

[Application management views in Configuration Manager](application-management-views-configuration-manager.md)
