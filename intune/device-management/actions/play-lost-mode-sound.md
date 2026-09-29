---
title: "Device action: play lost mode sound"
description: Learn how to use the Play lost device sound action in Microsoft Intune to trigger an audible alert on a lost, stolen, or misplaced device—helping users locate it quickly and securely.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
zone_pivot_groups: 22f7442d-9384-49c8-abff-aaa058b30589
---

# Device action: play lost mode sound

Microsoft Intune provides platform-specific device actions to help locate a lost or misplaced device by triggering an audible alert—even if the device is locked or silenced.

- On iOS/iPadOS, use the *play Lost Mode sound* action. This action is available when the device is in [Lost Mode](lost-mode.md) and supervised.
- On Android Enterprise devices, use the *Play lost device sound* action. This action is supported for corporate-owned devices enrolled with Android Enterprise.

These device actions are especially useful in environments where devices are shared or frequently moved—such as classrooms, labs, or enterprise workspaces. Playing a sound helps users or administrators locate the device quickly and securely, supporting recovery efforts when a device is lost.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - Android Enterprise corporate-owned dedicated (COSU)
> - Android Enterprise corporate-owned fully managed (COBO)
> - Android Enterprise corporate-owned work profile (COPE)
> - iOS/iPadOS in [Supervised Mode](../../device-enrollment/apple/enable-supervised-mode.md)

![](../../media/icons/16/configuration.svg) **Device configuration requirements**

::: zone pivot="ios"

> To use this action, make sure devices meet the following requirements:
>
> - Enable [Lost Mode](lost-mode.md)

::: zone-end

::: zone pivot="android"

> To use this action, make sure devices meet the following requirements:
>
> - Intune app is installed.

::: zone-end

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [School Administrator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#school-administrator)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Play sound to locate lost devices**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to play lost mode sound from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.

::: zone pivot="ios"

3. At the top of the device overview pane, locate the row of action icons. Select **Locate** &gt; **Play Lost Mode sound (supervised only)**.

::: zone-end

::: zone pivot="android"

3. At the top of the device overview pane, locate the row of action icons. Select **Locate** &gt; **Play lost device sound**.

::: zone-end

4. Select the duration for the sound to play on the device, and then select **Yes**.

## User experience

::: zone pivot="ios"

The sound plays until the user disables the sound or the duration you set expires.

::: zone-end

::: zone pivot="android"

If system notifications are enabled, the device displays a notification with a **Stop Sound** button. The alert plays for the configured duration or until a user on the device manually stops it using the notification.

Notification behavior might vary based on system settings. To configure system notifications, see [Android Enterprise device settings to allow or restrict features using Intune](../../device-configuration/templates/ref-device-restrictions-android-enterprise.md).

::: zone-end

## Reference links

- Microsoft Graph API: [playLostModeSound action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-playlostmodesound)
