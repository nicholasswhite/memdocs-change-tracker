---
title: "How to manage queries in Configuration Manager"
description: Learn how to manage your queries. Includes a table for detailed reference.
ms.date: "2019-04-29T00:00:00Z"
ms.subservice: core-infra
ms.topic: how-to
ms.collection: tier3
ms.service: configuration-manager
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
