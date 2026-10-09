---
title: "Integrate Better Mobile with Intune"
description: Integrate the third-party mobile threat defense solution of Better Mobile with Microsoft Intune.
ms.date: "2024-07-19T00:00:00Z"
ms.topic: how-to
author: lenewsad
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/7ebba99b-05c3-4387-8883-f7bbf6632cb8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/57eae307-c3a1-4cac-b645-1a899934bac8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/006ab567-b18c-4cf1-9a25-c24daa46ede1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/ee561821-1ac7-45a8-9409-6ba5eb7a5b97
---

# Integrate Better Mobile with Intune

Complete the following steps to integrate the Better Mobile Threat Defense solution with Intune.

## Before you begin

The following steps are to be completed in the Better Mobile admin console and will enable a connection to Better Mobile's service for both Intune enrolled devices (using device compliance) and unenrolled devices (using app protection policies).

Before starting the process of integrating Better Mobile with Intune, make sure you have the following:

- Microsoft Intune Plan 1 subscription
- Microsoft Entra admin credentials to grant the following permissions:

  - Sign in and read user profile
  - Access the directory as the signed-in user
  - Read directory data
  - Send device information to Intune
- Admin credentials to access the Better Mobile admin console.

### Better Mobile app authorization

The Better Mobile app authorization process follows:

- Allow the Better Mobile service to communicate information related to device health state back to Intune.
- Better Mobile syncs with Microsoft Entra Enrollment Group membership to populate its device's database.
- Allow the Better Mobile admin console to use Microsoft Entra single sign-on (SSO).
- Allow the Better Mobile app to sign in using Microsoft Entra SSO.

## To set up Better Mobile integration

1. Go to the Better Mobile admin console and sign in with your credentials.
2. Choose **Integration** &gt; **EMM/MDM** &gt; **ADD ACCOUNT**.

   ![Image of the Better Mobile admin console](media/setup-better-mobile/better_mobile_console.png)
3. Choose **Intune**.
4. Next to **ACCOUNT NAME**, type a descriptor.
5. In the **Microsoft Sign in** window, enter your Intune credentials.
6. In the **Permissions requested** window, choose **Accept**.
7. Search for the Microsoft Entra security groups that you want Better Mobile to sync devices from, and select them in the list. Then select **Continue**.
8. Select **Done**.
9. The **Add account** page reappears. Close the page.

## Next steps

- [Set up Better Mobile apps for enrolled devices](assign-apps.md)
- [Set up Better Mobile apps for unenrolled devices](add-apps-unenrolled-devices.md)
