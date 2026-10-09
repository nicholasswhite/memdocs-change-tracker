---
description: The following examples demonstrate various Microsoft Configuration Manager SQL view queries.
title: "How to See a Configuration Manager View by Using SQL Server"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: how-to
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

# How to See a Configuration Manager View by Using SQL Server

The following examples demonstrate various Microsoft Configuration Manager SQL view queries.

## Examples

#### To determine the display name of a resource type from the resource type number

- In SQL Server, query the Configuration Manager database with the following SQL statement:

```
select DisplayName from v_ResourceMap where ResourceType=5
```

#### To determine discovery properties for a particular resource type

- In SQL Server, query the Configuration Manager database with the following SQL statement:

```
select * from v_ResourceAttributeMap where ResourceType=5
```

#### To list the inventory groups for a particular resource type

- In SQL Server, query the Configuration Manager database with the following SQL statement:

```
select InvClassName from v_GroupMap where ResourceType = 5
```
