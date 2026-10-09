---
title: "How Configuration Manager collects diagnostics and usage data"
description: Learn about how Configuration Manager collects diagnostics and usage data about itself.
ms.date: "2021-08-10T00:00:00Z"
ms.subservice: core-infra
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/486161dc-fa28-4625-9b1c-1a21d690bc8d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/5dd28c86-729c-4723-ab5a-57e26fcec2a8
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
---

# How Configuration Manager collects diagnostics and usage data

*Applies to: Configuration Manager (current branch)*

To collect diagnostics and usage data for Configuration Manager, each primary site runs SQL Server queries on a weekly basis. In a multi-site hierarchy, the data is replicated to the central administration site.

At the top-level site of a hierarchy, the service connection point submits this information when it checks for updates. The mode of the service connection point determines how the data is transferred:

- **Online**: Once a week, the service connection point automatically sends diagnostics and usage data to the cloud service.
- **Offline**: You manually transfer diagnostics and usage data with the [service connection tool](../../servers/manage/use-the-service-connection-tool.md).

For more information, see [About the service connection point](../../servers/deploy/configure/about-the-service-connection-point.md).

Next, you can view diagnostic and usage data to confirm that your Configuration Manager hierarchy contains no sensitive information:

[How to view diagnostics and usage data](view-diagnostics-and-usage-data.md)

> [!TIP]
>
> The **ConfigurationManager** PowerShell module also collects usage data. For more information, see [Configuration Manager cmdlet library privacy statement](https://learn.microsoft.com/en-us/powershell/sccm/privacy-statement).
>
> Some of the tools that are included with Configuration Manager collect usage data. For more information, see [Diagnostic usage data for tools](tools.md).
