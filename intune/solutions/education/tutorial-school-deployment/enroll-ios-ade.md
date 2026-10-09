---
title: "Enroll devices with Automated Device Enrollment"
description: Learn how to automatically enroll devices through Apple School Manager with Automated Device Enrollment during Setup Assistant on iOS/iPadOS devices.
ms.date: "2024-05-02T00:00:00Z"
ms.topic: tutorial
author: scottbreenmsft
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/c6f99e62-1cf6-4b71-af9b-649b05f80cce
manager: laurawi
moniker_range_name: ''
ms.author: scbree
ms.service: microsoft-intune
ms.subservice: education
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3f56b378-07a9-4fa1-afe8-9889fdc77628
---

# Enroll devices with Automated Device Enrollment

Automated Device Enrollment through Apple School Manager is designed to simplify all parts of iOS devices lifecycle, from initial deployment through end of life. Using cloud-based services, Automated Device Enrollment can reduce the overall costs for deploying, managing, and retiring devices.

From the user's perspective, it only takes a few simple operations to make their device ready to use. The only interaction required from the end user is to set their language and regional settings, connect to a network, and depending on the profile type - verify their credentials. Everything beyond that is automated.

There are two types of enrollment:

- **User affinity**. This enrollment type is designed for devices that have only one user. In this scenario, the user is prompted for credentials during enrollment.
- **No user affinity**. This enrollment type is designed for shared devices and is common in lower grades. In this scenario, no credentials are required to enroll the device. For iPad devices, a configuration called Shared iPad can be applied that allows users to log in with their Managed Apple ID or use a temporary session.

For more information on configuring Automated Device Enrollment, see:

- [Intune](#tabpanel_1_intune)
- [Intune For Education](#tabpanel_1_intune-for-education)

<a id="tabpanel_1_intune"></a>



[Set up automated device enrollment in Intune](../../../device-enrollment/apple/setup-automated-ios.md).

<a id="tabpanel_1_intune-for-education"></a>



[Set up iOS device management](https://learn.microsoft.com/en-us/intune-education/setup-ios-device-management)

## Next steps

With the devices managed by Intune, you can use Intune to maintain them and report on their status.

[Next: Manage devices &gt;](manage-overview.md)
