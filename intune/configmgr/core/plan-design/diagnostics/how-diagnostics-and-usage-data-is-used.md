---
title: "How Microsoft uses Configuration Manager diagnostics and usage data"
description: Learn about how Microsoft uses the diagnostics and usage data that Configuration Manager collects.
ms.date: "2021-08-10T00:00:00Z"
ms.subservice: core-infra
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/cbe4ca68-43ac-4375-aba5-5945a6394c20
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/fc3f72c2-fb6f-4cea-95ee-b444e52254ee
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/f12cf087-582d-48ac-a085-0c19adf1e391
---

# How Microsoft uses Configuration Manager diagnostics and usage data

*Applies to: Configuration Manager (current branch)*

Diagnostic and usage data that Configuration Manager collects provides Microsoft nearly immediate feedback about how the product is working and is used to adjust future updates. Microsoft can also see configuration data that helps them engineer and test the configurations that you use in production. For example:

- The Windows server versions used on site servers
- Installed language packs
- The delta of the SQL Server schema against the product default

This data helps the engineering team plan future tests to make sure you have the best experience with the most common configurations. This data is crucial to quickly adjust and adapt with a frequent release cycle.

Equally important is how the diagnostics and usage data isn't used. Microsoft doesn't use this data for:

- Licensing audits, such as comparing customer usage against license agreements
- Auditing of products that are out of support
- Advertising based on available data such as feature usage or geolocation (time zone)

Microsoft uses available data to improve the product. For example:

- The initial support offered by the current branch of Configuration Manager limited the support timeline for Windows Server 2008 R2. Microsoft examined the usage data from customers who had upgraded to the Configuration Manager current branch. They then identified the need to revise and extend this timeline to support customers who still use this OS.
- Microsoft improved the prerequisite checks for installing an update. They removed obsolete rules, accounted for additional cases, and automatically remediated some issues.

Next, learn about how Configuration Manager collects diagnostics and usage data about itself:

[How Configuration Manager collects data](how-diagnostics-and-usage-data-is-collected.md)
