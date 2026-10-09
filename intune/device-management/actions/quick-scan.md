---
title: "Device action: quick scan"
description: Learn how to initiate on demand Microsoft Defender quick scan with Microsoft Intune.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
author: paolomatarazzo
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c671beaa-a830-4c9f-aceb-97379ee031ca
manager: laurawi
moniker_range_name: ''
ms.author: paoloma
ms.collection: M365-identity-device-management
ms.reviewer: mattcall
ms.service: microsoft-intune
ms.subservice: remote-actions
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/8921374c-4dbe-4ed0-b011-a39e18bfbd98
---

# Device action: quick scan

The *quick scan* action in Microsoft Intune enables IT administrators to start a targeted malware scan on managed Windows devices by using Microsoft Defender Antivirus. This action scans key system areas where threats commonly appear—such as memory, startup folders, and running processes—without performing a full system sweep.

Quick scans are especially useful for routine health checks, validating recent policy deployments, or responding to low-risk alerts. By triggering a scan remotely from the Intune admin center, IT teams can quickly assess device health and ensure protection is up to date—without waiting for the next scheduled scan or relying on user intervention.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platform:
>
> - Windows

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [Endpoint Security Manager](../../fundamentals/role-based-access-control/ref-built-in-roles.md#endpoint-security-manager)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Windows defender**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to initiate a quick scan from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, find the row of action icons. Select **Microsoft Defender** &gt; **Run quick malware scan**.

## Reference links

- Microsoft Graph API: [windowsDefenderScan action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-windowsdefenderscan)
- Configuration service provider (CSP) used to initiate the action: [Defender CSP](https://learn.microsoft.com/en-us/windows/client-management/mdm/defender-csp)
