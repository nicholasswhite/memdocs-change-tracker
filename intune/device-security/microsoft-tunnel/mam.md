---
title: "Microsoft Tunnel for Mobile Application Management"
description: Use Microsoft Tunnel for MAM with Android and iOS devices. Tunnel for MAM expands access to your organizational resources for devices that aren't or can't enroll with Microsoft Intune.
ms.date: "2024-10-10T00:00:00Z"
ms.topic: article
ms.subservice: suite
ms.collection:
- M365-identity-device-management
- sub-intune-suite
---

# Microsoft Tunnel for Mobile Application Management

When you use the Microsoft Tunnel VPN Gateway, you can extend Tunnel support by adding Tunnel for Mobile Application Management (MAM). Tunnel for MAM extends the Microsoft Tunnel VPN gateway to support devices that run Android or iOS, and that aren't enrolled with Microsoft Intune. With this solution, your users can use a single device that isn't enrolled with Intune to gain secure access to the organizations on-premises apps and resources using modern authentication, single sign-on, and Conditional Access. With Tunnel for MAM, your users can use their own device (BYOD) for both work and personal use, without having to grant the organization's IT department control over that device.

Before you begin, you must already have deployed the Microsoft Tunnel gateway. To learn more about Microsoft Tunnel gateway and how to install and configure it, see:

- [Learn about the Microsoft Tunnel VPN solution for Microsoft Intune](overview.md)
- [Identify the prerequisites to install and use the Microsoft Tunnel VPN solution for Microsoft Intune](prerequisites.md)
- [Install and configure Microsoft Tunnel VPN solution for Microsoft Intune](install.md)

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> - Android Enterprise
> - iOS/iPadOS

![](../../media/icons/16/licensing.svg) **Licensing requirements**

> This feature requires Microsoft Intune Plan 2 or an additional subscription. For licensing options, see [Microsoft Intune plans and pricing](https://aka.ms/MicrosoftIntunePricing) and [Microsoft 365 Security Enterprise Plans](https://www.microsoft.com/security/pricing/enterprise-plans).

The following table identifies key features for the supported platforms:

| Requirements and Features | Tunnel for Android | Tunnel for iOS |
| --- | --- | --- |
| Requirements: | - Company Portal app (sign-in not required)   - Defender for Endpoint app | - No Company Portal app or Defender for Endpoint app requirement |
| Features: | - VPN is provided via the Defender for Endpoint app:   --- Per App VPN   --- Device-wide VPN    - *Auto-launch*: VPN automatically starts on app launch | - VPN is provided via Tunnel for MAM SDK for iOS integration    - Per-App VPN. Tunnel connection is restricted to each targeted app    - *Auto-launch*: VPN automatically starts on app launch    - No Device-wide VPN    - Trusted root certificate support for on-premises CA trust |
| Line of Business app requirements | - Intune App SDK for Android    - Microsoft Authentication Library (MSAL) integration | - Intune App SDK for iOS    - Microsoft Authentication Library (MSAL) integration   --- Microsoft Entra App registration    - Tunnel for MAM SDK for iOS |
| Microsoft Edge browser support: | - *Strict Tunnel Mode*: When users sign in to Microsoft Edge with an organization account, if the VPN isn't connected, then **Strict Tunnel Mode** blocks internet traffic. When the VPN reconnects, internet browsing is available again.    - *Identity switch*: VPN connects when using a work or school account and disconnects when switching to a personal account or in-Private browsing.    - Device-wide and Per-App VPN support | - *Strict Tunnel Mode*: When users sign in to Microsoft Edge with an organization account, if the VPN isn't connected, then **Strict Tunnel Mode** blocks internet traffic. When the VPN reconnects, internet browsing is available again.    - *Identity switch*: VPN connects when using a work/school account and disconnects when switching to a personal account or in-Private browsing. |
| Third-party browser support: | - Only with device-wide VPN enabled | - None |

## Try the interactive demos

Try the following interactive demos to discover how Tunnel for MAM extends Microsoft Tunnel VPN Gateway to support Android and iOS devices that aren't enrolled with Intune.

- [Microsoft Tunnel for Mobile Application Management for Android](/ https:/regale.cloud/Microsoft/viewer/1896/microsoft-tunnel-for-mobile-application-management-for-android/index.html#/0/0)
- [Microsoft Tunnel for Mobile Application Management for iOS/iPadOS](/ https:/regale.cloud/Microsoft/viewer/1976/microsoft-tunnel-for-mobile-application-management-for-ios-ipados/index.html#/0/0)

## Related content

- [Learn about the Microsoft Tunnel VPN solution for Microsoft Intune](overview.md)
- [Use MAM Tunnel for Android](mam-android.md)
- [MAM Tunnel for iOS](mam-ios.md)
