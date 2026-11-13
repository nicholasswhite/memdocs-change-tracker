---
title: Automatic registration of existing devices
description: Automatically register existing devices with Windows Autopilot through Intune or another MDM service. Learn the
  requirements and how to convert targeted devices.
ms.date: '2026-10-30T00:00:00Z'
ms.topic: how-to
ms.collection:
  - M365-modern-desktop
  - m365initiative-coredeploy
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
  - ✅ <a href="https://learn.microsoft.com/hololens/hololens-release-notes" target="_blank">Windows Holographic</a>
author: madakeva
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4b132a0c-342a-42eb-91ff-8159e1ed413d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
moniker_range_name: ''
ms.author: madakeva
ms.service: windows-client
ms.subservice: autopilot
ms.suite: ems
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/f2b71146-ce8e-46a8-9965-8aa8b3aa8235
---

# Automatic registration of existing devices

## Requirements

An existing device can automatically register if it meets the following criteria:

- Runs a [supported version](https://learn.microsoft.com/en-us/windows/release-information/) of Windows
- Enrolled in a mobile device management (MDM) service such as Intune
- A corporate device that isn't already registered with Windows Autopilot

For devices that meet these requirements, the MDM service can request the hardware hash from the device. After it has the hardware hash, it can automatically register the device with Windows Autopilot.

For more information about how to automatically register devices for Windows Autopilot with Microsoft Intune, see [Create a Windows Autopilot deployment profile](profiles.md#create-a-windows-autopilot-deployment-profile) and review the description of the **Convert all targeted devices to Autopilot** setting. See the following example:

![Screenshot that shows how to convert all targeted devices.](images/convert-devices.png)

> [!NOTE]
>
> Using the **Convert all targeted devices to Autopilot** setting in the Windows Autopilot profile doesn't automatically convert existing hybrid Microsoft Entra devices in the assigned groups into Microsoft Entra devices. The setting only registers the devices in the assigned groups for the Windows Autopilot service. For more information, see [Create a Windows Autopilot deployment profile](profiles.md#create-a-windows-autopilot-deployment-profile).

## Windows Autopilot for existing devices

When you use the [Windows Autopilot for existing devices](existing-devices.md) scenario, you don't need to preregister devices with Windows Autopilot. Instead, use a configuration file (AutopilotConfigurationFile.json) that contains the Windows Autopilot profile settings. You can then register the device with Windows Autopilot by using the **Convert all targeted devices to Autopilot** setting.

## Related content

- [Registration overview](registration-overview.md)
