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
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
- https://authoring-docs-microsoft.poolparty.biz/devrel/7cbaac1e-1137-4825-819f-cd751d73c036
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/eda7d4a5-11e2-4d6f-b379-0d496f2a17a5
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
