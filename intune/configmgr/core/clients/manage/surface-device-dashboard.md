---
title: "Surface device dashboard in Configuration Manager"
description: Review information about Surface devices using the dashboard.
ms.date: "2021-11-15T00:00:00Z"
ms.topic: how-to
ms.subservice: core-infra
ms.collection: tier3
ms.custom: sfi-image-nochange
ms.service: configuration-manager
---

# Surface device dashboard in Configuration Manager

*Applies to: Configuration Manager (current branch)*

The Surface device dashboard gives you information about Surface devices found in your environment at a single glance.

## How to open

To open the Surface device dashboard, use the following steps:

1. Open the Configuration Manager console.
2. Select the **Monitoring** workspace.
3. To load the dashboard, select the **Surface Devices** node.

![An example view of the Surface device dashboard.](media/surface-device-dashboard.png)

## Review information

The Surface device dashboard shows three graphs:

- **Percent of Surface devices**: The percentage of Surface devices throughout your environment.

  ![Percent of Surface devices graph.](media/percent-surface-devices.png)
- **Surface Models**: The number of devices per Surface model. Hover over a graph section to see the percentage of Surface devices for that model.

  ![Surface models graph.](media/surface-models-hover.png)

  - Select a graph section to go through to a device list for that model.

    ![Surface model device list.](media/surface-model-device-list.png)
- **Top five firmware versions**: The top five firmware models in your environment. Hover over a graph section to see the number of Surface devices with that firmware version. Select a graph section to go through to a device list.

  ![Surface top five firmware versions graph.](media/surface-firmware-hover.png)

## Next steps

You can use Configuration Manager to deploy Surface firmware updates. For more information, see [Managing Surface driver updates](../../../sum/deploy-use/surface-drivers.md).

For more information about Surface devices, see the [Surface](https://www.microsoft.com/surface) website.
