---
title: "Integrate CrowdStrike Falcon for Mobile with Microsoft Intune"
description: How to set up CrowdStrike Falcon Threat Defense with Microsoft Intune to control mobile device access to your corporate resources.
ms.date: "2025-02-12T00:00:00Z"
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

# Integrate CrowdStrike Falcon for Mobile with Microsoft Intune

Complete the following steps to integrate the CrowdStrike Falcon for Mobile solution with Intune.

> [!NOTE]
>
> This Mobile Threat Defense vendor isn't supported for unenrolled devices.

## Before you begin

The instructions in this article are done in the [CrowdStrike Falcon for Mobile console](https://falcon.crowdstrike.com).

Before starting the process of integrating CrowdStrike Falcon with Intune, make sure you have the following configurations:

- Microsoft Intune Plan 1 subscription
- Microsoft Entra admin credentials to grant the following permissions:

  - Sign in and read user profile
  - Access the directory as the signed-in user
  - Read directory data
  - Send device information to Intune
- Admin credentials to access the CrowdStrike Falcon for Mobile console.

### CrowdStrike Falcon app authorization

The CrowdStrike Falcon app authorization process consists of the following steps:

- Allow the CrowdStrike Falcon for Mobile service to communicate information related to device health state back to Intune.
- CrowdStrike Falcon syncs with Microsoft Entra Enrollment Group membership to populate its device's database.
- Allow the CrowdStrike Falcon for Mobile console to use Microsoft Entra single sign-on (SSO).
- Allow the CrowdStrike Falcon app to sign in using Microsoft Entra SSO.

## Set up CrowdStrike Falcon for Mobile integration

CrowdStrike documents the integration steps at [Integrating Falcon for Mobile with Microsoft Intune for remediation actions](https://falcon.crowdstrike.com/documentation/page/odf8977b/integrating-falcon-for-mobile-with-microsoft-intune-for-remediation-actions). You must sign in with your CrowdStrike credentials before you can access this content.

## Related content

- [Set up CrowdStrike Falcon apps](assign-apps.md)
