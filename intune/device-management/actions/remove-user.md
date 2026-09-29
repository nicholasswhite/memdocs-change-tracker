---
title: "Device action: remove user"
description: Learn how to remove a user from a Shared iPad with Microsoft Intune.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
---

# Device action: remove user

The *remove user* device action in Microsoft Intune deletes a selected user's cached session from a Shared iPad. This helps free up storage, support privacy, and prepare the iPad for other users. The removed user can sign in again if needed.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - iPadOS (Shared iPad mode only)

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Manage shared device users**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to remove a user from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a Shared iPadOS device.
3. Select **Users**.
4. In the list, right-click the user that you want to remove, and then select **Remove user**.

## Reference links

- Microsoft Graph API: [deleteUserFromSharedAppleDevice action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-deleteuserfromsharedappledevice)
