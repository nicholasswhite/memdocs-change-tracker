---
title: "Device action: deprovision"
description: Learn how to deprovision a chromeOS device with Microsoft Intune.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
author: paolomatarazzo
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/68e4b2d8-b70c-4019-b49a-d1f8881e2aea
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: paoloma
ms.collection: M365-identity-device-management
ms.reviewer: mattcall
ms.service: microsoft-intune
ms.subservice: remote-actions
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/67b2ba1a-6f74-4044-a48a-f0f8ad076b8f
---

# Device action: deprovision

The *deprovision* device action in Microsoft Intune enables IT administrators to remove Google Admin policies from ChromeOS devices that are no longer in use by the organization.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - ChromeOS

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [School Administrator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#school-administrator)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Retire**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to deprovision a device from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, find the row of action icons. Select **Deprovision**. To confirm, select **Yes**.

After you deprovision a device, it remains in the Intune admin center and the Google Admin console. In the **System info** pane, the device status changes to **Deprovisioned**. The device can't be enrolled again until you restore it to factory settings. For more information about the deprovision action, such as how to select the best reason for deprovisioning, see the [Chrome Enterprise and Education Help documentation](https://support.google.com/chrome/a/answer/3523633).

## Reference links

- Microsoft Graph API: [deprovision action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-deprovision)
