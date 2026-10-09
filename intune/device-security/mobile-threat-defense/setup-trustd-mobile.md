---
title: "Integrate Trustd Mobile with Microsoft Intune"
description: How to set up Trustd Mobile Threat Defense with Microsoft Intune to control mobile device access to your corporate resources.
author: lenewsad
ms.author: lanewsad
ms.date: "2026-06-24T00:00:00Z"
ms.topic: how-to
ms.reviewer: ilwu
ai-usage: ai-assisted
ms.collection:
- M365-identity-device-management
- sub-mtd-apps
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/7ebba99b-05c3-4387-8883-f7bbf6632cb8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.service: microsoft-intune
ms.subservice: protect
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/006ab567-b18c-4cf1-9a25-c24daa46ede1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Integrate Trustd Mobile with Microsoft Intune

Complete the following steps to integrate the Trustd Mobile solution with Intune. The instructions in this article are performed in the [Trustd Mobile console](https://control.traced.app/devices/zero-trust/intune).

## Before you begin

Before starting the process of integrating Trustd Mobile with Intune, make sure you have the following configurations:

- Microsoft Intune Plan 1 subscription
- Microsoft Entra admin credentials to grant the following permissions:
  - Sign in and read user profile
  - Access the directory as the signed-in user
  - Read directory data
  - Send device information to Intune
- Admin credentials to access the Trustd Mobile console

## Trustd Mobile app authorization

The Trustd Mobile app authorization process consists of the following steps:

1. Go to the [Trustd Mobile console](https://control.traced.app/devices/zero-trust/intune) and sign in with your credentials.
2. Choose **Settings** from the top bar.
3. Choose **Integrations** from the left bar.
4. Under **Microsoft Intune**, select **Authorise now**.
5. Authenticate to Microsoft and add the Trustd Mobile Intune Connector app.

> [!IMPORTANT]
>
> To perform the Trustd Mobile integration setup, you must sign in with a Microsoft Entra user who has the Global Administrator role. This one-time setup operation uses the Global Administrator rights to grant permission in your organization for the Trustd Mobile apps to communicate with Intune.

## Set up Trustd Mobile integration

For step-by-step setup guidance, see [Microsoft Intune – Zero Trust Conditional Access](https://traced.app/getting-started-guide-unmanaged-customer/#step12) in the Trustd Mobile documentation.

## Related content

- [Mobile Threat Defense with Microsoft Intune](overview.md)
- [Enable mobile threat connectors in Intune](enable-connector.md)
