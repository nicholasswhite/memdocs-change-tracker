---
title: "How to manage queries in Configuration Manager"
description: Learn how to manage your queries. Includes a table for detailed reference.
ms.date: "2019-04-29T00:00:00Z"
ms.subservice: core-infra
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# How to manage queries in Configuration Manager

*Applies to: Configuration Manager (current branch)*

This article can help you manage queries in Configuration Manager.

For information about how to create queries, see [How to create queries](create-queries.md).

## Manage queries

In the **Monitoring** workspace, select **Queries**, select the query to manage, and then select a management task.

The following table provides information about the management tasks.

| Management task | Details |
| --- | --- |
| **Run** | Runs the selected query and displays the results in the Configuration Manager console. |
| **Install Client** | Opens the **Install Client Wizard**, which lets you install the Configuration Manager client on computers returned by the selected query.   This option isn't available for queries that return mobile devices, users, or user groups.    For more information about how to install Configuration Manager clients by using client push, see [Deploy clients to Windows computers](../../clients/deploy/deploy-clients-to-windows-computers.md). |
| **Export** | Opens the **Export Objects Wizard**. This wizard lets you export the query to a Managed Object Format (MOF) file that you can then import at another site. |
| **Move** | Opens the **Move Selected Items** dialog box. This dialog box lets you move the selected query to a folder that you previously created under the **Queries** node. |

## Next steps

[Create queries](create-queries.md)
