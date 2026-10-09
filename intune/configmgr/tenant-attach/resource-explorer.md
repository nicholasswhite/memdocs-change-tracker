---
title: "Tenant attach: Resource explorer in the admin center"
description: View hardware inventory for uploaded Configuration Manager devices using resource explorer in the admin center.
ms.date: "2022-07-11T00:00:00Z"
ms.topic: how-to
ms.subservice: core-infra
ms.collection: tier3
ms.custom: sfi-image-nochange
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/68e4b2d8-b70c-4019-b49a-d1f8881e2aea
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/67b2ba1a-6f74-4044-a48a-f0f8ad076b8f
---

# Tenant attach: Resource explorer in the admin center

*Applies to: Configuration Manager (current branch)*

The Microsoft Intune family of products is an integrated solution for managing all of your devices. Microsoft brings together Configuration Manager and Intune into a single console called **Microsoft Intune admin center**. From the Microsoft Endpoint Management admin center, you can view hardware inventory for uploaded Configuration Manager devices by using resource explorer.

[![Resource explorer in Microsoft Intune admin center](media/6479284-resource-explorer.png)](media/6479284-resource-explorer.png#lightbox)

## Prerequisites

The following items are required to use resource explorer from the admin center:

- All of the prerequisites for [Tenant attach: ConfigMgr client details](client-details.md).
- A supported version of Configuration Manager version and the corresponding version of the console installed.
  - Historical inventory data requires Configuration Manager version 2103, or later.
- Upgrade the target devices to the latest version of the Configuration Manager client.

## Permissions

The user account needs the following permissions:

- The **Read** permission for the device's **Collection** in Configuration Manager.
- The **Read Resource** permission for the device's **Collection** in Configuration Manager.
- An [Intune role](../../fundamentals/role-based-access-control/overview.md) assigned to the user

## Launch resource explorer

1. In a browser, go to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Devices** then **All Devices**.
3. Select a device that is synced from Configuration Manager via [tenant attach](device-sync-actions.md).
4. Select **Resource explorer** to view hardware inventory.
5. Search for or select a class to retrieve information from the client.

   [![Resource explorer with the motherboard class selected](media/6479284-resource-explorer-details.png)](media/6479284-resource-explorer-details.png#lightbox)

## Historical inventory data in resource explorer

*Applies to Configuration Manager 2103, or later*

Resource explorer can display a historical view of the device inventory in the Microsoft Intune admin center. When troubleshooting, having historical inventory data can provide valuable information about changes to the device.

1. From the Microsoft Intune admin center, select **Resource explorer**.
2. Select a class.
3. Enter a custom date in the date time picker to get historical inventory data.

[![Screenshot of choosing a date from Resource explorer in the Microsoft Intune admin center ](media/9546584-resource-explorer-historical-inventory.png)](media/9546584-resource-explorer-historical-inventory.png#lightbox)

## Close resource explorer

To close resource explorer and return to the device information, use the `X` icon in the top right of resource explorer.

[![Close resource explorer with the x icon in Microsoft Intune admin center](media/6479284-close-resource-explorer.png)](media/6479284-close-resource-explorer.png#lightbox)

## Next steps

[Troubleshoot resource explorer](troubleshoot-resource-explorer.md)
