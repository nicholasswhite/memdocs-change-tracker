---
title: "Query views in Configuration Manager"
description: Information about all the queries in the Configuration Manager hierarchy.
ms.date: "2019-04-30T00:00:00Z"
ms.subservice: sdk
ms.topic: reference


ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/cbe4ca68-43ac-4375-aba5-5945a6394c20
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
---

# Query views in Configuration Manager

Configuration Manager has only one query view, **v_Query**. It contains information about all the queries in the Configuration Manager hierarchy. The query ID, query name, comment, target class name, and the collection ID to which the query is limited, if applicable, are all listed.

The **v_Query** view can be joined to the **v_CollectionRuleQuery** collection view by using the **QueryID** column and to collection views by using the **LimitToCollectionID** column, which contains the same information as the **CollectionID** column in other views. It's also possible to join the query view to a security view so that the query name can be displayed when listing the class or instance permissions on the specific query object. An example is available in the section [Sample queries for queries in Configuration Manager](sample-queries-for-queries-configuration-manager.md).

## See also

[SQL Server views in Configuration Manager](sql-server-views-configuration-manager.md)
