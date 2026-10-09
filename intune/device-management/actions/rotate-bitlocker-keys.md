---
title: "Device action: BitLocker key rotation"
description: Learn how to rotate the BitLocker recovery key with Microsoft Intune.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
author: paolomatarazzo
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
---

# Device action: BitLocker key rotation

The *BitLocker key rotation* action in Microsoft Intune lets IT admins remotely refresh the recovery key for the operating system drive on BitLocker-encrypted Windows devices. This helps reduce the risk of unauthorized access if a recovery key has been used or potentially exposed.

Key rotation is especially useful in environments where devices are frequently serviced, reassigned, or exposed to support scenarios. For example, if a helpdesk technician shares a recovery key during a support call, you can rotate the key from Intune to ensure it can't be reused.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - Windows

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Help Desk Operator](../../fundamentals/role-based-access-control/ref-built-in-roles.md#help-desk-operator)
> - [Endpoint Security Manager](../../fundamentals/role-based-access-control/ref-built-in-roles.md#endpoint-security-manager)
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Rotate BitLockerKeys**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to rotate the BitLocker key from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, find the row of action icons. Select **Secure** &gt; **BitLocker key rotation**.
4. Select **Yes** to confirm the action.

## Reference links

- Configuration service provider (CSP) used to initiate the action: [BitLocker CSP](https://learn.microsoft.com/en-us/windows/client-management/mdm/bitlocker-csp#rotaterecoverypasswords)
- Microsoft Graph API: [rotateBitLockerKeys action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-rotateBitLockerKeys)
- [BitLocker overview](https://learn.microsoft.com/en-us/windows/security/operating-system-security/data-protection/bitlocker/)
