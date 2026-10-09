---
title: "Integrate Pradeo Mobile Threat Defense with Intune"
description: How to set up the Pradeo Mobile Threat Protection solution with Microsoft Intune to control mobile device access to your corporate resources.
ms.date: "2024-08-27T00:00:00Z"
ms.topic: how-to
author: lenewsad
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/ee561821-1ac7-45a8-9409-6ba5eb7a5b97
---

# Integrate Pradeo Mobile Threat Defense with Intune

Complete the following steps to integrate the Pradeo Mobile Threat Defense solution with Intune.

> [!NOTE]
>
> This Mobile Threat Defense vendor is not supported for unenrolled devices.

## Before you begin

> [!NOTE]
>
> The following steps are to be completed in the [Pradeo Security console](https://pradeo-security.com/).

The process of integrating Pradeo with Intune requires the following subscriptions and account permissions:

- Microsoft Intune Plan 1 subscription
- Microsoft Entra credentials to grant the following permissions:
  - Sign in and read user profile
  - Access the directory as the signed-in user
  - Read directory data
  - Send device information to Intune
- Admin credentials to access Pradeo Security console.

### Pradeo app authorization

The Pradeo app authorization process follows:

- Allow the Pradeo service to communicate information related to device health state back to Intune.
- Pradeo syncs with Microsoft Entra Enrollment Group membership to populate its device's database.
- Allow Pradeo admin console to use Microsoft Entra single sign-on (SSO).
- Allow the Pradeo app to sign in using Microsoft Entra SSO.

## To set up Pradeo integration

1. Go to [Pradeo Security console](https://pradeo-security.com/) and sign in with your credentials.
2. Choose **Administration - Enterprise Mobility Management** from the menu.
3. Choose the **Intune logo**.
4. In the **EMM (Enterprise mobility management) - Intune** window, under **Step 1**, choose the **Pradeo Connector** button.

   ![Screenshot of the Pradeo EMM Intune window](media/setup-pradeo/pradeo_setup.png)
5. In the Microsoft Intune connection window, enter your Intune credentials.
6. The Pradeo web page reopens. Under **Step 2**, choose the **Pradeo Device Health** button.
7. In the Pradeo-Intune Connector window, select **Accept**.
8. In the Pradeo device API connector window, select **Accept**.
9. The Pradeo web page reopens. Under **Step 3**, choose the **Connect to Microsoft** button.
10. In the Microsoft Intune authentication window, enter your Intune credentials.
11. When the message **Successful Integration** appears, integration is complete.

## Next steps

- [Set up Pradeo apps for enrolled devices](assign-apps.md)
