---
title: "Sample queries for endpoint protection in Configuration Manager"
description: Sample queries that show how to join the most common Endpoint Protection views to other views.
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

# Sample queries for endpoint protection in Configuration Manager

The following sample queries demonstrate how to join the most common Endpoint Protection views to other views.

## Joining endpoint protection and collection views

The following query lists the deployment state of the Endpoint Protection client on all computers by using the **v_GS_EPDeploymentState** view. For each computer, it also adds the client name and site code by joining by **ResourceID** to the **v_ClientCollectionMembers** view.

```sql
    SELECT   v_GS_EPDeploymentState_1.ResourceID, v_ClientCollectionMembers.Name, v_ClientCollectionMembers.SiteCode, 
                     v_GS_EPDeploymentState_1.LastMessageTime, v_GS_EPDeploymentState_1.DeploymentState, v_GS_EPDeploymentState_1.Error, 
                     v_GS_EPDeploymentState_1.ErrorCode
    FROM    v_GS_EPDeploymentState AS v_GS_EPDeploymentState_1 INNER JOIN
            v_ClientCollectionMembers ON v_GS_EPDeploymentState_1.ResourceID = v_ClientCollectionMembers.ResourceID
```

## See also

[Endpoint protection views in Configuration Manager](endpoint-protection-views-configuration-manager.md)
