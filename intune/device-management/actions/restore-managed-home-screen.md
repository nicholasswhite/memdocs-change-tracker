---
title: "Device action: restore Managed Home Screen"
description: Learn how to restore the Managed Home Screen with Microsoft Intune.
ms.date: "2026-04-21T00:00:00Z"
ms.topic: how-to
---

# Device action: restore Managed Home Screen

The *restore Managed Home Screen* device action in Intune re-enables the Managed Home Screen on a device that was previously suspended. When the Managed Home Screen is restored, the device will enforce the Managed Home Screen policies again, restricting access to only the apps and settings defined by those policies.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - Android Enterprise corporate-owned Fully Managed (COBO)
> - Android Enterprise corporate-owned Dedicated (COSU)

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [School Administrator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#school-administrator)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Restore Managed Home Screen**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

![](../../media/icons/16/configuration.svg) **Device configuration requirements**

> To run this action, the **Alarms &amp; Reminders** permission must be granted to the Managed Home Screen.
>
> For more information, see [Configure permissions for the Managed Home Screen (MHS) on Android Enterprise devices using Microsoft Intune](../../device-configuration/templates/configure-managed-home-screen-permissions-android.md).

## How to restore the managed home screen from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, find the row of action icons. Select **Remote actions** &gt; **Restore Managed Home Screen**.

## User experience

Once the Managed Home Screen is restored, the device will enforce the Managed Home Screen policies again, and the user will have access to the Managed Home Screen and apps.

## Reference links

- Microsoft Graph API: [managedDevice resource type](https://learn.microsoft.com/en-us/graph/api/resources/intune-devices-manageddevice)
- Microsoft Graph API: [restoreManagedHomeScreen action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-restoremanagedhomescreen)
