---
title: "Configuration Manager Schema Overview"
description: This article discusses the Configuration Manager Schema Overview.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: concept-article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/ced846cc-6a3c-4c8f-9dfb-3de0e90e2742
---

# Configuration Manager Schema Overview

Configuration Manager uses Windows Management Instrumentation (WMI) to manage its objects. Any managed object, such as a disk drive or a collection of computers, can be represented by an instance of a Configuration Manager class. Configuration Manager also includes classes that represent Configuration Manager features, such as software distribution. Collectively, these Configuration Manager classes are known as the Configuration Manager schema.

Configuration Manager uses a Microsoft SQL Server database to store managed object data. Both SQL Server and the WMI API can be used to view and manipulate Configuration Manager managed data. The SMS Provider acts as an intermediary between Configuration Manager site information and WMI by supplying both class and instance data.

## Server

The Configuration Manager classes that represent the Configuration Manager server schema are generally declared in the SMSProv.mof file. This file contains the base classes, static classes, and methods that the SMS Provider supports. Other class definitions, notably those that support inventory, are determined at run time by the SMS Provider. When requested, these class definitions are supplied to WMI. These are called run-time classes. The SMSProv.mof file is located in the \Bin\&lt;*Platform*&gt;\ directory under the Configuration Manager install directory.

For more information about using these Configuration Manager classes by using WMI or managed code, see [Objects overview](configuration-manager-objects-overview.md).

You can also use SQL Views for fast, read-only access to the Configuration Manager schema data. For more information, see [Configuration Manager Schema SQL Views](configuration-manager-schema-sql-views.md)

## Client

A number of Managed Object Format (MOF) files represent the client Configuration Manager schema. The client includes schemas that can be used for items such as inventory, policy, and software distribution management.

For more information about using client objects with WMI or managed code, see [About client WMI programming](../clients/programming/about-configuration-manager-wmi-programming.md).

## Classes

For more information about the classes that Configuration Manager supports, see [Configuration Manager Reference](../../reference/configuration-manager-reference.md).

## See Also

[Configuration Manager Schema View Mapping](configuration-manager-schema-view-mapping.md) [Configuration Manager Schema SQL Views](configuration-manager-schema-sql-views.md) [Configuration Manager SQL View Security](sql-view-security.md)
