---
title: Power Viewer Tool
description: Use the Power Viewer Tool to view the status of the power management feature on a Configuration Manager client.
ms.date: "2018-07-30T00:00:00Z"
ms.subservice: core-infra
ms.topic: how-to
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

# Power Viewer Tool

*Applies to: Configuration Manager (current branch)*

The Power Viewer tool is one of the [Configuration Manager tools](tools.md). Use it to view the status of the power management feature on a Configuration Manager client.

Run **PowerVwr.exe** as an administrator. When the tool launches, it displays the power capabilities and power settings of the local computer on the **Power Config** tab.

To view the power management data of a remote computer:

1. Go to the **File** menu, and click **Connect**.
2. Enter the **Computer** name, and a **Username** and **Password**, if necessary.

There are three tabs in Power Viewer:

- **Power Config**: View the power capabilities and power settings of the targeted computer.
- **Daily Activity**: View the daily activity charts of the client, which includes the following information:

  - **Computer on**: The power status of the computer in one day. Sleep mode is considered as power off.
  - **Monitor on**: On or off status of monitor in one day.
  - **User Active**: User activity information in one day.
- **Power Events**: View all of the daily power events. The client summarizes these events at 12:00 AM. This summarization generates data for the daily activity chart.
