---
title: "Redo Workplace Join for Android Enterprise devices"
description: Learn how to redo Workplace Join (re-WPJ) on an Android Enterprise device that's already enrolled in Intune but needs Azure AD registration completed.
ms.date: "2026-06-18T00:00:00Z"
ms.topic: how-to
ms.reviewer: grwilso
---

# Redo Workplace Join for Android Enterprise devices

This article describes how to complete Workplace Join (WPJ) on an Android Enterprise device that's already enrolled in Microsoft Intune. Use this guide if a user lands on the **Get Started** enrollment page but their device is already enrolled and they only need to redo the Workplace Join step.

## When does this happen

This scenario can occur when enrollment and Azure AD registration become out of sync. Common situations include:

- A user began web-based enrollment but didn't complete the Workplace Join step.
- A device migrated from the legacy custom DPC management stack to Android Management API, and the registration step didn't complete.
- A user's work account was removed or re-added on the device without fully unenrolling.

## Before you begin

This edge case can affect devices enrolled in any of the following Android Enterprise management types:

- Personally owned work profile (web-based enrollment)
- Personally owned work profile (app-based enrollment)
- Corporate-owned work profile
- Fully managed
- Dedicated

Before starting, confirm that the device is already enrolled in Intune (visible in the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) under **Devices** &gt; **All devices**), the user has their work account credentials available, and Microsoft Authenticator is installed on the device.

## Redo Workplace Join

If a user's device registration becomes out of sync with enrollment, have the user complete the following steps to redo Workplace Join and restore access to work resources.

1. Open the app used to enroll the device (Microsoft Intune for web-based enrollment or Intune Company Portal for app-based enrollment).
2. Select the notification to complete Workplace Join.
3. Follow the on-screen instructions to register the device.
4. Return to the work app, such as Microsoft Outlook or Microsoft Teams, and try accessing it again.

If the user can access work resources again, Workplace Join completed successfully.

## Related content

- [Set up enrollment of Android Enterprise personally owned work profile devices](setup-personal-work-profile.md)
- [Android Management API for personally owned work profiles](android-management-api-overview.md)
- [Troubleshoot Android Enterprise device enrollment](https://learn.microsoft.com/en-us/troubleshoot/mem/intune/device-enrollment/troubleshoot-android-enrollment)
