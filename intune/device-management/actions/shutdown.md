---
title: "Device action: shut down"
description: Learn how to shutdown Apple devices with Microsoft Intune.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
---

# Device action: shut down

With the *shut down* action, IT administrators can remotely power off managed devices. This action doesn't prompt or warn the user before the device powers down.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - iOS/iPadOS in [Supervised Mode](https://learn.microsoft.com/en-us/intune/intune-service/remote-actions/device-supervised-mode)
> - macOS

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [School Administrator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#school-administrator)
> - [Endpoint Security Manager](../../fundamentals/role-based-access-control/ref-built-in-roles.md#endpoint-security-manager)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Shut down**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to shut down a device from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, find the row of action icons. Select **Remote actions** &gt; **Shut down** &gt; **Yes**.

> [!NOTE]
>
> iOS/iPadOS devices that are Passcode-locked will not rejoin a Wi-Fi network after restarting. After restarting, the device might not be able to communicate with the server.

## Reference links

- Microsoft Graph API: [shutDown action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-shutdown)
