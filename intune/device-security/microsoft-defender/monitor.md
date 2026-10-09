---
title: "Monitor device status for Microsoft Defender for Endpoint with Microsoft Intune"
description: Learn how to monitor device compliance and onboarding status for Microsoft Defender for Endpoint with Microsoft Intune in the admin center.
ms.date: "2026-04-28T00:00:00Z"
ms.topic: how-to
ms.custom: msecd-doc-authoring-1012
author: lenewsad
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/07bb3e10-d135-43ff-bc8b-360497cb39fa
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/8b9ae643-2e85-42b8-beb2-eef4bae8c4bc
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: lanewsad
ms.collection:
- M365-identity-device-management
- sub-secure-endpoints
ms.reviewer: laarrizz
ms.service: microsoft-intune
ms.subservice: protect
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/12e559b9-eaf6-4aee-9af7-62334e15f863
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/e047e27d-b5f3-43a8-b4b0-4f6dca95e7c9
---

# Monitor device status for Microsoft Defender for Endpoint with Microsoft Intune

When you integrate Microsoft Intune and Microsoft Defender for Endpoint, you can monitor device compliance and onboarding status in the Microsoft Intune admin center to verify that devices are protected.

## Monitor device compliance

Monitor the state of devices that have the Microsoft Defender for Endpoint compliance policy.

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Devices** &gt; **Compliance**. On the **Monitor** tab, select **Noncompliant devices**.
3. Find your Microsoft Defender for Endpoint policy in the list, and see which devices are compliant or noncompliant.

For more information about reports, see [Intune reports](../../device-management/reports/overview.md).

## View onboarding status

To view the onboarding status of your Intune-managed devices:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Select **Endpoint security** &gt; **Overview**.

   The default *Summary* tab includes a **Windows devices onboarded onto Microsoft Defender for Endpoint** visualization report that displays the count of devices reporting status from the Defender for Endpoint sensor.

## Next step

- [Enforce compliance for Microsoft Defender for Endpoint with Conditional Access in Intune](overview.md)
