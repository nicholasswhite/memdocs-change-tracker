---
title: "Get the App Bundle ID for Your Policies in Microsoft Intune"
description: Get the app bundle ID in Microsoft Intune for Android, iOS/iPadOS, macOS, and Windows apps. Use the bundle ID in your app policies, device configuration profiles, enrollment policies, and compliance policies in Microsoft Intune.
ms.date: "2024-04-30T00:00:00Z"
ms.topic: how-to
ms.reviewer:
---

# Get the App Bundle ID for Your Policies in Microsoft Intune

When you add an app to Intune or use the built-in apps, the bundle ID of the app is also added. This bundle ID identifies the app, and you can use the bundle ID in your policies.

For example, you can use the bundle ID in an Intune device configuration profile to allow or block specific apps.

Applies to:

- Android
- iOS/iPadOS
- macOS
- Windows

This article lists the steps to get the app bundle IDs using the Intune admin center.

## Get the app bundle ID

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Apps** &gt; **All Apps**.
3. Select **Columns**.

   ![Screenshot that shows how to select the Columns option in All Apps in Microsoft Intune and the Intune admin center.](media/collect-bundle-ids/all-apps-column.png)
4. In the list, select **App identifier** &gt; **Apply**.

   ![Screenshot that shows how to select the App Bundle ID column in All Apps in Microsoft Intune and the Intune admin center.](media/collect-bundle-ids/columns-select-app-identifier.png)
5. The **App identifier** column shows the bundle ID of the app.

## Related articles

- [Add apps to Microsoft Intune](deployment/index.md)
- [Bundle IDs for built-in iOS and iPadOS apps you can use in Intune](../device-configuration/templates/ref-bundle-ids-ios.md)
- [Add built-in apps to Microsoft Intune](deployment/add-built-in.md)
