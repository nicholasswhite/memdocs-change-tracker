---
title: "Device action: rotate local admin password"
description: Learn how to rotate the local admin password on Windows and macOS devices with Microsoft Intune.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
zone_pivot_groups: 2fce401c-16eb-4314-8d26-844d8612f9c5
---

# Device action: rotate local admin password

The *rotate local admin password* action in Microsoft Intune lets IT admins manually rotate the password of a device's local administrator account. This helps improve security by refreshing credentials outside the scheduled rotation defined by the Microsoft Local Administrator Password Solution (LAPS). It's especially useful when responding to potential compromise, conducting audits, or resetting access during support scenarios.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This action supports the following platforms:
>
> - macOS [enrolled via Automated Device Enrollment (ADE)](../../device-enrollment/apple/setup-automated-macos.md)
> - Windows (corporate-owned)

![](../../media/icons/16/configuration.svg) **Device configuration requirements**

::: zone pivot="windows"

> To use this action, make sure devices meet the following requirements:
>
> - Are Microsoft Entra joined or Hybrid Entra joined.
> - Have Windows LAPS configured and actively backing up the local admin password to Microsoft Entra ID.
>
> For more information, see [What is Windows LAPS?](https://learn.microsoft.com/en-us/windows-server/identity/laps/laps-overview).

::: zone-end

::: zone pivot="macos"

> To use this action, make sure devices meet the following requirements:
>
> - The local admin account must be configured in the ADE profile before enrollment.
>
> For more information, see [Configure support for macOS ADE local account with LAPS](../../device-security/laps/setup-macos.md).

::: zone-end

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To run this action, use an account with at least one of the following roles:
>
> - [Custom role](../../fundamentals/role-based-access-control/create-custom-role.md) that includes:
>   - The permission **Remote tasks/Rotate Local Admin Password**
>   - Permissions that provide visibility into and access to managed devices in Intune (for example, Organization/Read, Managed devices/Read)

## How to rotate the local admin password from the Intune admin center

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, find the row of action icons. Select **Secure** &gt; **Rotate Local admin password**.

## Reference links

- Microsoft Graph API: [rotatelocaladminpassword action](https://learn.microsoft.com/en-us/graph/api/intune-devices-manageddevice-rotatelocaladminpassword)

::: zone pivot="windows"

- Configuration service provider (CSP) used to initiate the action: [LAPS CSP](https://learn.microsoft.com/en-us/windows/client-management/mdm/laps-csp)

::: zone-end

- [Manually rotate passwords with Windows LAPS](../../device-security/laps/deploy-policy.md#manually-rotate-passwords)
