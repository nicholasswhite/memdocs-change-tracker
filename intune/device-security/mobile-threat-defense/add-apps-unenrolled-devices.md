---
title: Add Mobile Threat Defense apps to unenrolled devices
description: Add Mobile Threat Defense apps to unenrolled devices by device users.
ms.date: "2024-08-20T00:00:00Z"
ms.topic: how-to
author: lenewsad
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/5686b492-7c45-4088-8291-ecc0458747d3
- https://authoring-docs-microsoft.poolparty.biz/devrel/a3955c7b-f5ee-420d-aff5-d7119738f38b
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: lanewsad
ms.collection:
- M365-identity-device-management
- sub-mtd-apps
ms.reviewer: ilwu
ms.service: microsoft-intune
ms.subservice: protect
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/838f4f15-80c1-4d49-b873-501fe4ed2d28
- https://authoring-docs-microsoft.poolparty.biz/devrel/b31948f4-2f38-404b-ac93-c3c8c5b3ae33
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
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
