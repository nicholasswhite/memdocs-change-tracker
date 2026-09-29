---
title: Add Mobile Threat Defense apps to unenrolled devices
description: Add Mobile Threat Defense apps to unenrolled devices by device users.
ms.date: "2024-08-20T00:00:00Z"
ms.topic: how-to
---

# Add Mobile Threat Defense apps to unenrolled devices

By default, when using Intune app protection policies with Mobile Threat Defense, Intune does the work to guide the end user on their device to install and sign in to all required apps to enable the connections with the relevant services.

End users need the Microsoft Authenticator (iOS) to register their device, and the Mobile Threat Defense (both Android and iOS) to receive notifications when a threat is identified in their mobile devices, and to receive guidance to remediate the threats.

Optionally, you can use Intune to add and deploy the Microsoft Authenticator, and Mobile Threat Defense (MTD) apps as well.

> For unenrolled devices, you **do not need an iOS app configuration policy** that sets up the Mobile Threat Defense for iOS app you use with Intune. This is a key difference compared to Intune enrolled devices.

## Configure Microsoft Authenticator for iOS via Intune (optional)

When using Intune app protection policies with Mobile Threat Defense, Intune guides the end user to install, sign in to, and register their device with the Microsoft Authenticator (iOS).

However, should you wish to make the app available to end users via the Intune Company Portal, see the instructions for [adding iOS store apps to Microsoft Intune](../../app-management/deployment/add-store-ios.md). Use this [Microsoft Authenticator - iOS App Store URL](https://itunes.apple.com/us/app/microsoft-authenticator/id983156458?mt=8) when completing the **Configure app information** section. Don't forget to [assigning app to groups with Intune](../../app-management/deployment/assign-groups.md) as the final step.

> [!NOTE]
>
> For iOS devices, you need the [Microsoft Authenticator](https://learn.microsoft.com/en-us/azure/multi-factor-authentication/end-user/microsoft-authenticator-app-how-to) so users can have their identities checked by Microsoft Entra. The Intune Company Portal works as the broker on Android devices so users can have their identities checked by Microsoft Entra.

## Making Mobile Threat Defense apps available via Intune (optional)

When you use Intune app protection policies with Mobile Threat Defense, Intune guides the end user to install and sign in to the required Mobile Threat Defense client app.

However, should you wish to make the app available to end users via the Intune Company Portal, you can follow the steps provided in the following sections. Make sure you're familiar with the process of:

- [Adding an app into Intune](../../app-management/deployment/index.md)
- [Assigning an app with Intune](../../app-management/deployment/assign-groups.md)

## Next steps

- [Enable the Mobile Threat Defense connector in Intune for unenrolled devices](enable-unenrolled-devices.md)
