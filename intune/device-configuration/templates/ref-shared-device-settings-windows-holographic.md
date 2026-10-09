---
title: "Windows Holographic for Business settings to manage shared devices using Intune"
description: Add and use Windows Holographic for Business to configure devices that are shared, or used by multiple users in Microsoft Intune. See a list of the Account Management settings and what they do on the devices, including Microsoft HoloLens.
ms.date: "2024-04-16T00:00:00Z"
ms.topic: reference
author: paolomatarazzo
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/05616262-6974-4662-ac87-15adf94b9c3a
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: paoloma
ms.collection: M365-identity-device-management
ms.service: microsoft-intune
ms.subservice: configuration
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/25c95491-bd10-484c-89ce-1fa29173d007
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Windows Holographic for Business settings to manage shared devices using Intune

Windows Holographic for Business devices, like the Microsoft HoloLens, can be used by multiple users. Devices that have multiple users are called shared devices, and are a part of mobile device management (MDM) solutions.

Users can sign in to these shared devices with a guest account. As they use the device, they only get access to features you allow.

This article describes the settings you use in a Windows Holographic for Business device configuration profile in Microsoft Intune. When the profile is created in Intune, you then deploy or assign the profile to device groups in your organization. You can also assign this profile to a device group with mixed device types and OS versions.

For more information on this feature in Intune, see [Control access, accounts, and power features on shared PC or multi-user devices](configure-shared-device.md). For more information on the Windows CSP, see [AccountManagement CSP](https://learn.microsoft.com/en-us/windows/client-management/mdm/accountmanagement-csp).

## Before your begin

- [Create a Windows shared multi-user device configuration profile](configure-shared-device.md).
- When you create a Windows shared user device configuration profile, there are more settings than what's listed in this article. The settings in this article are supported on Windows Holographic for Business devices.

## Shared multi-user device settings

> [!NOTE]
>
> Devices that run Windows Holographic for Business, including the Microsoft HoloLens, only support the **Account management** settings. If you configure any of the other settings shown in Intune, including **Shared PC mode**, it has no impact on these devices.

- **Account management**: Choose if accounts are automatically deleted. Your options:
  - **Not configured** (default): Intune doesn't change or update this setting.
  - **Enabled**: Automatically deletes local accounts created by guests, and accounts in on-premises Active Directory and Microsoft Entra ID. When a user signs off the device, or when system maintenance runs, these accounts are deleted.

    Also enter:

    - **Account Deletion**: Choose when accounts are deleted:
      - **At storage space threshold**
      - **At storage space threshold and inactive threshold**
      - **Immediately after log-out**

    Also enter:

    - **Start delete threshold(%)**: Enter a percentage (0-100) of disk space. When the total disk/storage space drops below the value you enter, the cached accounts are deleted. It continuously deletes accounts to reclaim disk space. Accounts that are inactive the longest are deleted first.
    - **Stop delete threshold(%)**: Enter a percentage (0-100) of disk space. When the total disk/storage space meets the value you enter, the deleting stops.
  - **Disable**: The local, Active Directory, and Microsoft Entra accounts created by guests stay on the device, and aren't deleted.

## Related articles

- [Assign the profile](../assign-device-profile.md) and [monitor its status](../monitor-device-profile.md).
- See the shared user device settings for [Windows](ref-shared-device-settings-windows.md).
