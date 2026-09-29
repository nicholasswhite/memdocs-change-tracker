---
title: "Set up device enrollment with Apple School Manager"
description: Learn how to set up Microsoft Intune with Apple School Manager for corporate-owned iOS/iPadOS devices.
ms.date: "2026-04-29T00:00:00Z"
ms.topic: how-to
---

# Set up device enrollment with Apple School Manager

Set up Microsoft Intune to enroll Apple mobile devices purchased through [Apple School Manager](https://school.apple.com/). Using Intune with Apple School Manager, you can enroll large numbers of devices without ever touching them. When a student or teacher turns on the device, Apple Setup Assistant runs with preconfigured settings and the device enrolls into management.

## Prerequisites

To enable Apple School Manager enrollment, you use both the Microsoft Intune admin center and Apple School Manager portal.

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This enrollment method supports the following platforms:
>
> - iOS/iPadOS
> - tvOS
> - visionOS
>
> Devices must be added to [Apple School Manager](http://school.apple.com). You need a list of serial numbers or a purchase order number to assign devices in Apple School Manager. tvOS and visionOS devices enroll without user affinity and are enrolled as corporate-owned devices with configuration delivered through custom configuration profiles.

![](../../media/icons/16/tenant-administration.svg) **Tenant configuration requirements**

> - Get an [Apple mobile device management (MDM) push certificate](create-mdm-push-certificate.md).
> - Set up the [MDM Authority](../../fundamentals/setup-mdm-authority.md).
> - If using Active Directory Federation Services (AD FS), user affinity requires [WS-Trust 1.3 Username/Mixed endpoint](https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ff608241(v=ws.10)). For more information, see [Get ADFS endpoint](https://learn.microsoft.com/en-us/powershell/module/adfs/get-adfsendpoint).

Apple School Manager enrollment can't be used with the [device enrollment manager](../setup-enrollment-manager.md) account.

## Next steps

This series of articles describes how to set up Microsoft Intune for devices purchased through Apple School Manager.

1. 🡺 Prerequisites (*You are here*)
2. [Get an Apple token for school devices](school-manager-step-1.md)
3. [Create an Apple enrollment policy](school-manager-step-2.md)
4. [Sync and distribute devices](school-manager-step-3.md)
