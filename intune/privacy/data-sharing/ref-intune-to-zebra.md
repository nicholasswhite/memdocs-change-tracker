---
title: Data Intune sends to Zebra
description: List of data that Intune sends to Zebra.
ms.date: "2023-12-07T00:00:00Z"
ms.topic: reference
ms.reviewer: jieyan
author: paolomatarazzo
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/7cf8f81d-2989-4e5d-aa91-5191d10a3323
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: paoloma
ms.collection:
- M365-identity-device-management
- privacy
- sub-data-privacy
ms.service: microsoft-intune
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/1cb9c90f-9a3f-4389-8367-0a20c542621f
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Data Intune sends to Zebra

When Zebra LifeGuard Over-the-Air (LG OTA) is enabled for your tenant, Microsoft Intune establishes a connection with Zebra and shares the following data with Zebra:

The following table lists the data that Microsoft Intune sends to Google when device management is enabled on a device:

| Data sent to Zebra | Used for | Example |
| --- | --- | --- |
| Serial number | Used to prove ownership of device against a known service contract with Zebra, determine current state of the device, and for the Android update process. | Unique identifier, example format: 124411614K0593 |
| Deployment settings | Used to deliver Android updates. | - Device Model: TC8300 - Update type: Custom Time zone offset in minutes: 300 - BSP (Board Support Package): 11.15.05.00 - OS Version: 11 - Patch Number: U20 - Schedule mode: Latest - Schedule duration in days: 20 - Download network type: Wifi - Download start date and time: - 2022-03-25T15:04:51.8607086Z - Installation start date and time: - 2022-03-25T15:04:51.8607086Z - Installation window start time: 19:00:00 - Installation window end time: 19:00:00 - Minimum Battery level percentage: 30 - Require device to be on charger: true |

To stop using Zebra services with Microsoft Intune and delete the data, you must both disconnect from Zebra LifeGuard OTA in Microsoft Intune, and also delete the data from your Zebra account by filing a customer request with Zebra.
