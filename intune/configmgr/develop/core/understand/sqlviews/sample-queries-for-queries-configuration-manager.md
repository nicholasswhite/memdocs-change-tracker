---
title: "Sample queries for the query view in Configuration Manager"
description: Sample queries that show how the query view can be joined to a security view.
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

# Sample queries for the query view in Configuration Manager

The following sample query demonstrates how the query view can be joined to a security view. In most cases, the **v_Query** view won't be used in reports.

## Joining query and security views

The following query lists the query ID, query name, user name, and instance permissions for the user on the query object. The **v_Query** view is joined to the **v_UserInstancePermNames** security view by using the **QueryID** from **v_Query** and **InstanceKey** from **v_UserInstancePermNames**. Because there might be other secured objects with the same value as the **InstanceKey** (for example, MCM00001 could be a custom query or a package), the query also filters specifically for query objects by using the WHERE clause and an **ObjectKey** value of 7.

```sql
    SELECT Q.QueryID, Q.Name AS QueryName, UIP.UserName, UIP.PermissionName 
    FROM v_Query Q INNER JOIN v_UserInstancePermNames UIP 
    ON Q.QueryID = UIP.InstanceKey 
    WHERE UIP.ObjectKey = 7 
    ORDER BY Q.Name, UIP.UserName 
```

## See also

[Query views in Configuration Manager](query-views-configuration-manager.md)
