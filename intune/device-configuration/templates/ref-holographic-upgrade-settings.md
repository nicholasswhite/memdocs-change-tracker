---
title: "Upgrade HoloLens (1st gen) devices running Windows Holographic to Windows Holographic for Business"
description: Upgrade HoloLens (first gen) to Windows 10 Holographic for Business using a device configuration profile in Microsoft Intune.
ms.date: "2025-10-14T00:00:00Z"
ms.topic: reference
---

# Upgrade HoloLens (1st gen) devices running Windows Holographic to Windows Holographic for Business

Microsoft Intune includes many settings to help manage and protect your devices. This article lists and describes the settings to upgrade HoloLens (1st gen) devices running Windows Holographic to Windows Holographic for Business.

This article applies to:

- Microsoft HoloLens (1st gen) devices

> [!IMPORTANT]
>
> HoloLens (1st gen) devices can run Windows Holographic and Windows Holographic for Business. All HoloLens 2 devices use Windows Holographic for Business. You don't need to update the edition of any HoloLens 2 device, regardless of the device SKU.

As part of your mobile device management (MDM) solution, use these settings to upgrade your HoloLens (1st gen) Windows Holographic devices. For the Microsoft HoloLens (1st gen), you can purchase the Commercial Suite to get the required license for the upgrade. For more information, see [Unlock Windows Holographic for Business features](https://learn.microsoft.com/en-us/hololens/hololens1-upgrade-enterprise).

As an Intune administrator, you can create and assign these settings to your devices.

For more information on this feature, see [Upgrade Windows editions or enable S mode](configure-edition-upgrade-windows.md).

## Before you begin

- On October 14, 2025, [Windows 10 reached end of support](https://learn.microsoft.com/en-us/lifecycle/announcements/windows-10-end-of-support) and won't receive quality and feature updates. Windows 10 is an **allowed** version in Intune. Devices running this version can still enroll in Intune and use eligible features, but functionality won't be guaranteed and can vary.
- [Create a Windows client edition upgrade and mode switch device configuration profile](configure-edition-upgrade-windows.md#create-the-profile).
- When you create a Windows client edition upgrade and mode switch device configuration profile, there are more settings than what's listed in this article. The settings in this article are supported on Windows Holographic for Business devices.

## Edition upgrade

- **Edition to upgrade to**: Select **Windows 10 Holographic for Business**.
- **License File**: Browse to and select the XML license file that was provided to you.

  ![In Intune, enter the XML file name that includes the Holographic for Business license information.](media/ref-holographic-upgrade-settings/holographic-edition-upgrade.png)

## Related articles

- [Assign the profile](../assign-device-profile.md), and [monitor its status](../monitor-device-profile.md).
- Create edition upgrade profiles for [Windows](ref-edition-upgrade-settings-windows.md) devices.
