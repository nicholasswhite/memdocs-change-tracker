---
title: "Inventory views in Configuration Manager"
description: Hardware and software inventory information about the clients, files, and products, in the Configuration Manager hierarchy.
ms.date: "2019-04-30T00:00:00Z"
ms.subservice: sdk
ms.topic: reference


ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Inventory views in Configuration Manager

Inventory views contain hardware and software inventory information about the clients, files, products, and so forth, in the Configuration Manager hierarchy. Configuration Manager collects inventory data when you enable the Hardware Inventory Client Agent or Software Inventory Client Agent. Because you can configure which hardware inventory to collect during the hardware inventory scan cycle and which file types to scan for during the software inventory scan cycle, each site will have a unique set of inventory that is collected.

For each Configuration Manager site, it's possible to retrieve a list of the hardware and software inventory schema to determine exactly what is inventoried. The articles in this section provide examples of how to do get the hardware and software inventory lists, and detailed information about the typical Configuration Manager SQL views.

## In This Section

- [Hardware inventory views in Configuration Manager](hardware-inventory-views-configuration-manager.md)
- [Software inventory views in Configuration Manager](software-inventory-views-configuration-manager.md)
- [Asset intelligence views in Configuration Manager](asset-intelligence-views-configuration-manager.md)

## See also

[SQL Server views in Configuration Manager](sql-server-views-configuration-manager.md)
