---
title: Data transfers between sites
description: Learn how Configuration Manager moves data between sites, and how you can manage the transfer of the data across your network.
ms.date: "2019-08-09T00:00:00Z"
ms.subservice: core-infra
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
---

# Data transfers between sites

*Applies to: Configuration Manager (current branch)*

Configuration Manager uses *file-based replication* and *database replication* to transfer different types of information between sites. Learn about how Configuration Manager moves data between sites, and how you can manage the transfer of data across your network.

## Types of replication

### File-based replication

Configuration Manager uses file-based replication to transfer file-based data between sites in your hierarchy. This data includes applications and packages that you want to deploy to distribution points in child sites. It also handles unprocessed discovery data records that the site transfers to its parent site and then processes.

For more information, see [File-based replication](file-based-replication.md).

### Database replication

Configuration Manager database replication uses SQL Server to transfer data. It uses this method to merge changes in its site database with the information from the database at other sites in the hierarchy.

For more information, see [Database replication](database-replication.md).

For help with troubleshooting SQL Server replication, see [Troubleshoot SQL Server replication](https://learn.microsoft.com/en-us/intune/configmgr/core/servers/manage/replication/overview).

## See also

[Monitor replication](../../servers/manage/monitor-replication.md)
