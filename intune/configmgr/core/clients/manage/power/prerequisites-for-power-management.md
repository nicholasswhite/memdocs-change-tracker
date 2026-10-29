---
title: "Prerequisites for power management in Configuration Manager"
description: Get the prerequisites for power management in Configuration Manager.
ms.date: "2016-10-06T00:00:00Z"
ms.subservice: core-infra
ms.topic: article
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

# Prerequisites for power management in Configuration Manager

*Applies to: Configuration Manager (current branch)*

Power management in Configuration Manager has external dependencies and dependencies within the product.

## Dependencies external to Configuration Manager

The following table lists the dependencies external to Configuration Manager for using power management.

| Dependency | More information |
| --- | --- |
| Client computers must be able to support the required power states | To use all features of power management, client computers must be able to support the sleep, hibernate, wake from sleep, and wake from hibernate actions. You can use the **Power Capabilities** report to determine if computers can support these actions. For more information, see [Power Capabilities report](monitor-and-plan-for-power-management.md#BKMK_Capabilites) in the topic [How to monitor and plan for power management](monitor-and-plan-for-power-management.md). |

## Configuration Manager dependencies

The following table lists the dependencies within Configuration Manager for using power management.

| Dependency | More Information |
| --- | --- |
| Power management must be enabled before you can create and monitor power plans. | For information about how to enable and configure power management, see [Configuring power management](configuring-power-management.md). |
| Reporting services point | You must configure a reporting services point before you can view power management reports. For more information, see [Introduction to reporting](../../../servers/manage/introduction-to-reporting.md). |
