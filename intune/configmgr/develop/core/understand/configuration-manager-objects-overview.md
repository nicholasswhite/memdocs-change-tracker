---
title: "Configuration Manager Objects Overview"
description: The Configuration Manager objects are instances of Configuration Manager-specific WMI classes managed by the SMS Provider.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: concept-article
ms.collection: tier3
ms.service: configuration-manager
---

# Configuration Manager Objects Overview

The Configuration Manager objects are instances of Configuration Manager-specific Windows Management Instrumentation (WMI) classes that are managed by the SMS Provider. The Configuration Manager object class categories are described in the following table.

| Configuration Manager Object Class Category | Description |
| --- | --- |
| Software distribution | Objects associated with the software distribution feature of Configuration Manager, such as advertisement, collection, package, and program objects. |
| Scheduling | Organizes scheduled Configuration Manager events, such as inventory updates. |
| Site | Contains information about Configuration Manager sites. |
| Security | Describes the permissions granted to users and user groups to operate on specific Configuration Manager-secured objects, such as program and package objects. |
| Query | Describes Configuration Manager site database queries. |
| Resource | Populated when Configuration Manager discovers potential client computers, users, user groups, and other types of objects within the boundaries of the site. |
| Inventory | Provides the structure for inventory operations on Configuration Manager client systems, users, and user groups. |
| Software metering | Describes the metered Configuration Manager resources, such as program files. |
| Status and summarizer | Indicates the status of Configuration Manager sites, components, and software distribution operations. |
| Collected files | Contains information about files collected from clients. |

## DebugView

To show SMS Provider object property values in the Configuration Manager console results pane, start the console with the following command line:

&lt;InstallationDirectory&gt;\Microsoft.ConfigurationManagement.exe /SMS:DebugView=1

For more information, see [Configuration Manager console command-line options](../../../core/servers/manage/admin-console.md#command-line-options).

## See Also

[Configuration Manager Association Classes](association-classes.md) [Configuration Manager Bit Field Properties](configuration-manager-bit-field-properties.md) [Configuration Manager console command-line options](../../../core/servers/manage/admin-console.md#command-line-options) [Configuration Manager Date and Time Formats](date-and-time-formats.md) [Configuration Manager Embedded Objects](embedded-objects.md) [Configuration Manager Extended WMI Query Language](extended-wmi-query-language.md) [Objects overview](configuration-manager-objects-overview.md) [Configuration Manager Lazy Properties](configuration-manager-lazy-properties.md) [About errors](about-configuration-manager-errors.md) [Configuration Manager Object Security](configuration-manager-object-security.md) [Configuration Manager Special Queries](special-queries.md)
