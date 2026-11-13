---
title: "Software updates planning guide for managed macOS devices in Microsoft Intune"
description: Guidance and advice for administrators that create and manage software updates for macOS devices using Microsoft Intune. Use this article to help manage software updates on your organization-owned devices, including how to create policies, manage updates, and review update status.
ms.date: "2025-07-23T00:00:00Z"
ms.topic: how-to
author: iye-ms
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/a3955c7b-f5ee-420d-aff5-d7119738f38b
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
moniker_range_name: ''
ms.author: iye
ms.service: microsoft-intune
ms.subservice: protect
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/b31948f4-2f38-404b-ac93-c3c8c5b3ae33
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Software updates planning guide for managed macOS devices in Microsoft Intune

Keeping your devices current with updates is critical. Admins must do what they can to reduce risk of security events, and reduce this risk with minimal disruption to the business &amp; users.

Intune has built-in policies that can manage software updates. For macOS devices, you can use Intune to manage device updates, configure when devices are updated, and review the device update status.

Use this article as an admin guide for your enrolled and managed macOS devices. This information can help you manage software updates on your organization-owned devices.

This article applies to:

- macOS devices enrolled in Intune

> [!TIP]
>
> - If your devices are personally owned, then go to the [software updates admin guide for personal devices](../byod-planning-guide.md).
> - Apple has deprecated MDM‑based software update workloads and removed the related commands with OS 27. Microsoft recommends using declarative device management (DDM) to manage and install Apple software updates. For more information about this transition, see the [Intune Customer Success blog: Move to declarative device management for Apple software updates](https://techcommunity.microsoft.com/blog/intunecustomersuccess/support-tip-move-to-declarative-device-management-for-apple-software-updates/4432177).

## Before you begin

To install updates faster and avoid delays, make sure the devices are:

- Powered on; not shut down but can be can a sleep state
- Plugged in
- Connected to Internet

## Manage updates with policies

✅ Do create policies that update your devices.

By default, users receive notifications and/or see the latest updates available on their devices (Settings &gt; General &gt; Software Updates). Users can choose to download and install updates whenever they want.

They can also change the update behavior using the Automatic Updates feature on the device (Settings &gt; Software Updates):

![The operating system default update settings and controls on a macOS Apple device.](media/planning-guide-macos/default-update-settings-macos-device.png)

When users install their own updates (instead of admins managing the updates), it can disrupt user productivity and business tasks. For example:

- Users can apply updates that your organization hasn't approved. This situation can cause issues with application compatibility, or changes to the operating system or user experience that disrupt device use.
- Users can avoid applying updates that are required for security or app compatibility reasons. This delay can leave the devices at risk and/or prevent them from being able to function.
- Users can disable checking for new updates entirely.

Because of these potential issues, Microsoft recommends that you evaluate your use case scenarios and deploy policies to manage the update experience to minimize risk and disruption to your business.

## Admin steps for organization owned devices

To update macOS devices owned by your organization, Microsoft recommends the following features. You can also use these features as a starting point for your own update strategy.

### ✅ Use DDM-managed software updates on macOS 14 and newer

On macOS 14 and newer devices, use Apple's declarative device management (DDM) to install a specific update by an enforced deadline.

DDM is the modern way to manage settings. The independent nature of DDM provides an improved user experience, as the device handles the entire software update lifecycle. It prompts users that an update is available and also downloads the update, prepares the device for the installation, &amp; installs the update.

Don't use the MDM-based software update policy settings on these devices, as Apple deprecated the MDM policies.

The DDM settings are configurable in the [Intune settings catalog](../../device-configuration/settings-catalog/index.md). For more information, go to [Managed software updates with the settings catalog](index.md).

### ✅ Configure Software Update Settings for user update experience

The [Intune settings catalog](../../device-configuration/settings-catalog/index.md) includes settings to help manage software updates. Create a policy that:

- Configures how users can interact with update behavior on the device, including automatic downloads and app updates.
- Prevents end users from disabling update checks.
- Configures the device to check for updates and prompt users regularly.

Use these settings together with DDM update enforcement in [Configure update policies for Apple devices](index.md). End users might still need to take action to finish some updates, depending on your configured deadlines and user experience settings.

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Devices &gt; Manage devices &gt; Configuration &gt; Settings catalog &gt; Declarative Device Management &gt; Software Update Settings**.
2. Configure Software Update Settings to control automatic update behavior and user interaction on the device. Common settings include:

   - **Automatic Download**: True
   - **Automatically Install App Updates**: True
   - **Automatically Install MacOS Updates**: True
   - **Automatic Check Enabled**: True
   - **Critical Update Install**: True

For more information on the settings catalog, including how to create a settings catalog policy, go to [Use the settings catalog to configure settings](../../device-configuration/settings-catalog/index.md).

##### End user experience

This policy locks these settings so users can't change them. On the device, the software update settings are greyed out:

![The software update settings are greyed out after the Intune settings catalog update policy applies to a macOS Apple device.](media/planning-guide-macos/update-settings-with-settings-catalog-policy-macos.png)

### ✅ Consider using the Nudge community tool

This tool is optional, and can help you **manage the end user experience**.

A popular tool within the Microsoft macOS admin community is Nudge. [Nudge is an open source community tool](https://github.com/macadmins/nudge) that encourages end users to install macOS updates. It provides a rich configuration experience for admins.

When Nudge is configured and deployed, end users see the following sample message when their device is ready to be updated. End users can also choose to update the device or defer the update:

[![A sample Nudge community tool message when a software update is available a macOS Apple device.](media/planning-guide-macos/nudge-sample-notification-message-macos.png)](media/planning-guide-macos/nudge-sample-notification-message-macos.png#lightbox)

There's also a [sample script and Intune configuration policy](https://github.com/microsoft/shell-intune-samples/tree/master/macOS/Apps/Nudge) for Nudge in the Microsoft shell script repository. This script includes everything you need to get started with Nudge. Make sure you update the `.mobileconfig` file with your values.

### ✅ Use built-in reporting for update status

After the update policies are deployed, in the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), you can use the reporting feature to check the status of the updates.

For each device, you can see update status using Apple software update reporting:

- **Reports** &gt; **Device management** &gt; **Apple updates**
- **Devices** &gt; **Monitor** &gt; **Apple software update failures**

[![Use the built-in reporting to check the update status of a macOS Apple device in the Microsoft Intune admin center.](media/planning-guide-macos/device-update-category-status.png)](media/planning-guide-macos/device-update-category-status.png#lightbox)

## Related articles

- [Software updates planning guide for BYOD and personal devices in Microsoft Intune](../byod-planning-guide.md)
- [Software updates planning guide for managed Android Enterprise devices in Microsoft Intune](../android/planning-guide.md)
- [Software updates planning guide and scenarios for supervised iOS/iPadOS devices in Microsoft Intune](planning-guide-ios-ipados.md)
