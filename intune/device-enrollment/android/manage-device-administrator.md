---
title: "Android device administrator enrollment"
description: Use Android device administrator with Intune to manage devices.
ms.date: "2024-10-28T00:00:00Z"
ms.topic: how-to
ms.reviewer: esalter
---

# Android device administrator enrollment

> [!IMPORTANT]
>
> Android device administrator (DA) management is deprecated and no longer available for devices with access to Google Mobile Services (GMS). If you currently use DA management, we recommend switching to another Android management option. Support and help documentation remain available for some Android 15 and earlier devices without GMS. For more information, see [Ending support for Android device administrator on GMS devices](https://techcommunity.microsoft.com/t5/intune-customer-success/microsoft-intune-ending-support-for-android-device-administrator/ba-p/3915443).

Android device administrator (sometimes referred to *legacy* Android management and released with Android 2.2) is a way to manage Android devices. However, improved management functionality is available with [Android Enterprise](https://www.android.com/enterprise/management/) in [countries/regions where Android Enterprise is available](https://support.google.com/work/android/answer/6270910). Google deprecated Android device administrator management in 2020. Intune is ending support for device administrator devices with access to Google Mobile Services at the end of 2024.

Therefore, we advise against enrolling new devices using the device administrator process described here and we also recommend that you migrate devices off of device administrator management.

For information about using device administrator when Google Mobile Services is unavailable, see [How to use Intune in environments without Google Mobile Services](../../app-management/manage-without-gms.md).

If you still decide to have users enroll their Android devices with device administrator management, continue to the next section.

## Set up device administrator enrollment

1. To prepare to manage mobile devices, you must set the mobile device management (MDM) authority to **Microsoft Intune**. See [Set the MDM authority](../../fundamentals/setup-mdm-authority.md) for instructions. You only need to configure this setting in your tenant once.
2. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
3. Go to **Devices** &gt; \*\*Enrollment.
4. Select the **Android** tab.
5. Under **Android device administrator**, choose **Personal and corporate-owned devices with device administration privileges**.
6. Select the checkmark next to **Use device administrator to manage devices**.
7. [Tell your users how to enroll their devices](../../user-help/enrollment/enroll-company-portal-android.md).

After a user enrolls, you can begin managing their devices in Intune, including [assigning compliance policies](../../device-security/compliance/ref-android-administrator-settings.md), [managing apps](../../app-management/overview.md), and more.

For information about other user tasks, see these articles:

- [Microsoft Intune planning guide](../../fundamentals/planning-guide.md)
- [Android device enrollment overview](../../user-help/enrollment/benefits-android.md)

## Block device administrator enrollment

To block Android device administrator devices, or to block only personally owned Android device administrator devices from enrollment, see [Set device type restrictions](../restrictions.md).

## Microsoft Teams certified Android devices

[Microsoft Teams certified Android devices](https://learn.microsoft.com/en-us/microsoftteams/devices/teams-ip-phones) should continue being managed with device administrator management until [AOSP user-associated](setup-aosp-corporate-user-associated.md) management becomes available for these devices.

To unenroll a Microsoft Teams-certified Android device you manage with Android device administrator, you must:

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/).
2. Deselect the Intune license from the Teams account for the Android device.

After you remove an Intune license, there's a 30 day grace period, during which the device still functions. The device must sign in again after this step to avoid enrolling in Intune under device administrator management again.

## Limitations

The limitations in this section apply to devices managed with device administrator.

Private space is a feature introduced with Android 15 that lets people create a space on their device for sensitive apps and data they want to keep hidden.

- The private space is considered a personal profile. Microsoft Intune doesn't support mobile device management within the private space or provide technical support for devices that attempt to enroll the private space.
- Users might try to create a work profile-like experience on their devices by enrolling only the private space, leading to partial device management. Microsoft Intune doesn't provide support for this scenario. To avoid this issue, we recommend using [personal work profile management](setup-personal-work-profile.md) or [corporate-owned work profile management](setup-corporate-work-profile.md) instead of device administrator management.
- After a user enrolls their personal device, if they attempt to enroll the private space, Intune will initiate the personal work profile enrollment flow. However, in this scenario the enrollment process will fail without any notification.

## Next steps

- [Assign compliance policies](../../device-security/compliance/ref-android-administrator-settings.md)
- [Managing apps](../../app-management/overview.md)
