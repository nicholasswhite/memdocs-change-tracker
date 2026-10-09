---
title: "About Configuration Manager Queries"
description: Create and run the queries that are accessible in the Configuration Manager console under Queries.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: concept-article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8b896464-3b7d-4e1f-84b0-9bb45aeb5f64
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1d2d671-9549-46e8-918c-24349120dbf5
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# About Configuration Manager Queries

You can create and run the queries that are accessible in the Configuration Manager console under **Queries**.

The queries can be used to locate objects in a Configuration Manager site that match your query criteria. These objects include items such as specific types of computers or user groups. Queries can return most types of Configuration Manager objects, including sites, collections, packages, and saved queries themselves. However, queries are most useful for extracting information that is related to resource discovery, inventory data, and status messages.

> [!NOTE]
>
> For more information, see [Introduction to queries](../../../core/servers/manage/introduction-to-queries.md).

## SMS_Query

Configuration Manager queries are defined by `SMS_Query` object instances. The query is a WQL query and is defined in the `Expression` property. For more information about WQL, see [Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md).

Each query has a unique identifier assigned to it by the SMS Provider and can be used to get a specific query. For information about running a query, see [How to Run a Configuration Manager Query](how-to-run-a-query.md).

You can also create queries by creating instances of `SMS_Query`. When you create a query, it is displayed in the Configuration Manager console under **Queries**. If you want to, you can limit the results returned to those resources that belong to a specific collection. For more information about creating queries, see [How to Create a Configuration Manager Query](how-to-create-a-configuration-manager-query.md).

## See Also

[Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md)

[Configuration Manager Result Sets](result-sets.md)

[Configuration Manager Special Queries](special-queries.md)

[How to Create a Configuration Manager Query](how-to-create-a-configuration-manager-query.md)

[How to Run a Configuration Manager Query](how-to-run-a-query.md)

[SMS_Query](../../reference/core/clients/manage/sms_query-server-wmi-class.md)
