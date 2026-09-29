---
title: "Features in Configuration Manager technical preview version 1911"
description: Learn about new features available in the Configuration Manager technical preview branch version 1911.
ms.date: "2019-11-05T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ROBOTS: NOINDEX
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 1911

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 1911. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Microsoft Configuration Manager

Configuration Manager is now part of the Microsoft Intune family of products.

![Microsoft Configuration Manager](media/4960084-endpoint-manager-logo.png)

Microsoft Intune family of products is an integrated solution for managing all of your devices. Microsoft brings together Configuration Manager and Intune, without a complex migration, and with simplified licensing. Continue to leverage your existing Configuration Manager investments, while taking advantage of the power of the Microsoft cloud at your own pace.

The following Microsoft management solutions are all now part of the **Microsoft Intune** brand:

- [Configuration Manager](https://learn.microsoft.com/en-us/configmgr)
- [Intune](https://learn.microsoft.com/en-us/mem/fundamentals/account-sign-up)
- [Desktop Analytics](../../../../device-updates/windows/monitor-compatibility.md)
- [Windows Autopilot](../../../../../autopilot/enrollment-autopilot.md)
- Other features in the [Device Management Admin Console](https://techcommunity.microsoft.com/t5/enterprise-mobility-security/microsoft-intune-rolls-out-an-improved-streamlined-endpoint/ba-p/937760)

For more information, see the following posts from Brad Anderson, Microsoft corporate vice president for Microsoft 365:

- [Announcement blog post](https://aka.ms/cmannounce)
- [Vision paper](https://aka.ms/MEMVisionPaper)
- [Announcement summary video](https://youtu.be/GS7oNPInFuw)

## Microsoft Connected Cache support for Intune Win32 apps

When you enable Microsoft Connected Cache on your Configuration Manager distribution points, they can now serve Microsoft Intune Win32 apps to co-managed clients.

> [!NOTE]
>
> Configuration Manager current branch version 1906 included [Delivery Optimization In-Network Cache](../../plan-design/hierarchy/microsoft-connected-cache.md), an application installed on Windows Server that's still in development. Starting in technical preview branch version 1911 this feature is now called **Microsoft Connected Cache**.
>
> When you install Connected Cache on a Configuration Manager distribution point, it offloads Delivery Optimization service traffic to local sources. Connected Cache does this behavior by efficiently caching content at the byte range level.

### Prerequisites

#### Client

- Update the client to the latest version.
- The client device needs to have at least 4 GB of memory.

  > [!TIP]
  >
  > Use the following group policy setting: Computer Configuration &gt; Administrative Templates &gt; Windows Components &gt; Delivery Optimization &gt; **Minimum RAM capacity (inclusive) required to enable use of Peer Caching (in GB)**.

#### Site

- Enable Connected Cache on a distribution point. For more information, see [Delivery Optimization In-Network Cache](../../plan-design/hierarchy/microsoft-connected-cache.md).
- The client and the Connected Cache-enabled distribution point need to be in the same boundary group.
- Enable the following client settings in the [**Delivery Optimization**](../../clients/deploy/about-client-settings.md#delivery-optimization) group:

  - **Use Configuration Manager Boundary Groups for Delivery Optimization Group ID**
  - **Enable devices managed by Configuration Manger to use Microsoft Connected Cache servers for content download**
- Enable the pre-release feature **Client apps for co-managed devices**. For more information, see [Pre-release features](../../servers/manage/pre-release-features.md).
- Enable co-management, and switch the **Client apps** workload to **Pilot Intune** or **Intune**. For more information, see the following articles:

  - [Workloads - Client apps](../../../comanage/workloads.md#client-apps)
  - [How to enable co-management](../../../comanage/how-to-enable.md)
  - [Switch workloads to Intune](../../../comanage/how-to-switch-workloads.md)

    If in pilot, add the client to the pilot collection for Client Apps.

#### Intune

- This feature only supports the Intune Win32 app type.

  - Create and assign (deploy) a new app in Intune for this purpose. (Apps created before Intune version 1811 don't work.) For more information, see [Intune Win32 app management](../../../../app-management/deployment/win32.md).
  - The app needs to be at least 100 MB in size.

    > [!TIP]
    >
    > Use the following group policy setting: Computer Configuration &gt; Administrative Templates &gt; Windows Components &gt; Delivery Optimization &gt; **Minimum Peer Caching Content File Size (in MB)**.

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md)
