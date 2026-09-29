---
title: "Device management in Microsoft Intune"
description: "Understand how to manage enrolled devices from the Devices area of the Microsoft Intune admin center, including device details, actions, inventory, scripts, reports, and integrations."
ms.date: "2026-07-05T00:00:00Z"
---

# Device management in Microsoft Intune

After devices enroll in Microsoft Intune, you manage them from the **Devices** area of the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431). From one place, you can review the devices in your organization, inspect the information Intune collects from each one, run remote actions, deploy scripts, monitor health through reports, and connect Intune to other services.

This article introduces the **Devices** area and explains how its sections are organized, so you know where to go for a given task. For step-by-step guidance, follow the links to the detailed articles in each section.

## Find your managed devices

To view the devices you manage, sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) and select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices). The **All devices** list shows every enrolled device, along with key columns such as operating system, ownership, compliance state, and last check-in. You can filter and sort the list, or select a platform-specific view (for example, [**Windows**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesWindowsMenu/%7E/windowsDevices)) to narrow the results.

Select any device in the list to open its device details page.

## Understand the device page

When you select a device, its **Overview** page opens with a command bar of [device actions](actions/index.md), an **Essentials** summary of key identifiers (compliance state, ownership, model, OS, serial number, Intune device name, scope tags, and primary user), and these tabs:

- **Monitor** — the status of the device's configuration policies, compliance, managed apps, and Endpoint Analytics score.
- **Properties** — the settings you can edit. See [Edit device properties](inventory-and-status/edit-device-properties.md).
- **Device details** — read-only hardware and inventory information. See [View device details](inventory-and-status/device-details.md).
- **Device action status** — the requested, in-progress, and recently completed [device actions](actions/index.md) for the device.

A navigation pane provides more views, grouped under **Tools** (such as device inventory, device query, BitLocker recovery keys, and remediations) and **Reports** (such as discovered apps, app configuration, device compliance, device configuration, and managed apps).

## Sections of the Devices area

The **Devices** area organizes device management into the following sections.

### Device actions

Respond to devices remotely, without physical access—wipe or retire a lost device, sync policies, restart, run a malware scan, rotate recovery keys, and more. Available actions depend on the platform and ownership. For the full list, see [Device actions](actions/index.md).

### Device inventory and organization

Review the data Intune collects from each device, and organize your devices for management:

- [View device details](inventory-and-status/device-details.md) and hardware inventory.
- [View ChromeOS device information](inventory-and-status/chrome-enterprise-details.md).
- [Edit device properties](inventory-and-status/edit-device-properties.md), such as ownership, notes, and scope tags.
- [Rename a device](inventory-and-status/rename-device.md).
- [Change a device's primary user](inventory-and-status/find-primary-user.md).
- [Create and assign device categories](create-device-categories.md).
- [Manage specialty devices](specialty-devices.md).

### Scripts and remediations

Extend management beyond built-in settings by running your own code on managed devices. Use the [Intune Management Extension](tools/management-extension-windows.md) to add [PowerShell scripts for Windows](tools/run-powershell-scripts-windows.md) or [shell scripts for macOS](tools/run-shell-scripts-macos.md), and use [remediations](tools/deploy-remediations.md) to detect and fix issues at scale.

### Reports

Monitor the health, compliance, and activity of your devices. Start with the [reports overview](reports/overview.md) or [export report data by using Graph APIs](reports/export-graph-apis.md).

### Integrations

Connect Intune to other services and tools, including the [Surface Management Portal](tools/surface-management-portal.md), [ServiceNow](tools/setup-servicenow.md), and [TeamViewer](tools/setup-teamviewer.md).

## Next steps

- [View device details](inventory-and-status/device-details.md)
- [Device actions](actions/index.md)
- [Microsoft Intune reports](reports/overview.md)
