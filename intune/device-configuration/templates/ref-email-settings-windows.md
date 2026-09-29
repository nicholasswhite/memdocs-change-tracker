---
title: "Email profile settings for Windows devices in Microsoft Intune"
description: Create a device configuration email profile that that uses Exchange servers, and retrieves attributes from Microsoft Entra ID. You can also enable SSL, and synchronize email and schedules on Windows 10/11 client devices using Microsoft Intune.
ms.date: "2026-06-23T00:00:00Z"
ms.topic: reference
ms.reviewer: sheetg
---

# Email profile settings for Windows devices in Microsoft Intune

> [!NOTE]
>
> Intune might support more settings than the settings listed in this article. Not all settings are documented, and won't be documented. To see the settings you can configure, create a device configuration policy, and select **Settings catalog**. For more information, go to [settings catalog](../settings-catalog/index.md).

In Microsoft Intune, you can create and configure an email profile to connect to an Exchange email server, choose how users authenticate, use S/MIME for encryption, and more. The email profile uses the native or built-in email app on the device, and users can connect to their organization email.

This article describes some of the settings you can configure. You can create a device configuration profile to assign or deploy these email settings to your iOS/iPadOS devices.

## Prerequisites

![](../../media/icons/16/devices.svg) **Device platform requirements**

> This feature supports the following platform:
>
> - Windows

![](../../media/icons/16/rbac.svg) **Roles requirements**

> To configure this policy and start collecting inventory data from devices, use an account with at least one of the following roles:
>
> - Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) with an account that has the **[Policy and Profile Manager](../../fundamentals/role-based-access-control/ref-built-in-roles.md#policy-and-profile-manager)** built-in role. For more information on the built-in roles, go to [Role-based access control for Microsoft Intune](../../fundamentals/role-based-access-control/overview.md).

![](../../media/icons/16/configuration.svg) **Device configuration requirements**

> - Deploy your [email app](configure-email.md).
> - Create a [Windows e-mail device configuration profile](configure-email.md).

## Email settings

- **Email server**: Enter the host name of your Exchange server. For example, enter `outlook.office365.com`.
- **Account name**: Enter the display name for the email account. This name is shown to users on their devices. For example, enter `Contoso corporate email`.
- **Username attribute from Microsoft Entra ID**: This name is the attribute Intune gets from Microsoft Entra ID. Intune dynamically generates the username that this profile uses. Your options:

  - **User Principal Name**: Gets the name, such as `user1` or `user1@contoso.com`.
  - **Primary SMTP address**: Gets the name in email address format, such as `user1@contoso.com`.
  - **sAM Account Name**: Requires the domain, such as `domain\user1`. Also enter:
    - **User domain name source**: Select **Microsoft Entra ID** or **Custom**.

      When getting the attributes from Microsoft Entra ID, also enter:

      - **User domain name attribute from Microsoft Entra ID**: Choose to get the **Full domain name** or the **NetBIOS name** Microsoft Entra attribute of the user.

      When using **Custom** attributes, also enter:

      - **Custom domain name to use**: Enter a value that Intune uses for the domain name, such as `contoso.com` or `contoso`.
- **Email address attribute from Microsoft Entra ID**: Intune gets this attribute from Microsoft Entra ID. Choose how the email address for the user is generated. Make sure your users have email addresses that match the attribute you select. Your options:

  - **User principal name**: Uses the full principal name as the email address, such as `user1@contoso.com` or `user1`.
  - **Primary SMTP address**: Uses the primary SMTP address to sign in to Exchange, such as `user1@contoso.com`.

### Security

- **SSL**: **Enable** uses Secure Sockets Layer (SSL) communication when sending emails, receiving emails, and communicating with the Exchange server. **Disable** doesn't require SSL.

### Synchronization

- **Amount of email to synchronize**: Select the number of days of email that you want to synchronize. When set to **Not configured** (default), Intune doesn't change or update this setting. Select **Unlimited** to synchronize all available email.
- **Sync schedule**: Select the schedule for devices to synchronize data from the Exchange server. You can also select **As Messages arrive**, which synchronizes data as soon as it arrives. Or, select **Manual** so the device user starts the synchronization.

  When set to **Not configured** (default), Intune doesn't change or update this setting.

### Content type to sync

Select the content types that you want to synchronize to devices. Your options:

- **Contacts**: **On** syncs the contacts. **Off** doesn't automatically sync the contacts. Users manually sync.
- **Calendar**: **On** syncs the calendar. **Off** doesn't automatically sync the contacts. Users manually sync.
- **Tasks**: **On** syncs the tasks. **Off** doesn't automatically sync the tasks. Users manually sync.

## Related articles

- Configure the email settings on [Android Enterprise](ref-email-settings-android-enterprise.md) and [iOS/iPadOS](ref-email-settings-ios.md).
- [Learn more about the email settings in Intune](configure-email.md).
- [Assign the profile](../assign-device-profile.md), and [monitor its status](../monitor-device-profile.md).
