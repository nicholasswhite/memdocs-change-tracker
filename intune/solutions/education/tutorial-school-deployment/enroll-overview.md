---
title: Device enrollment overview
description: Learn about the different options to enroll Windows devices in Microsoft Intune.
ms.date: "2024-05-02T00:00:00Z"
ms.topic: tutorial
zone_pivot_groups: platforms-windows-ios
author: scottbreenmsft
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: scbree
ms.service: microsoft-intune
ms.subservice: education
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Device enrollment overview

![The device lifecycle for Intune-managed devices - enrollment](media/shared/enroll.png)

In this section you will:

- Enroll your devices into Intune

Select one of the following options to learn the next steps about the enrollment method you chose:

::: zone pivot="windows"

- [Automatic Intune enrollment via Microsoft Entra join](enroll-entra-join.md)
- [Automatic Intune enrollment with provisioning packages](enroll-package.md)
- [Automatic Intune enrollment with Windows Autopilot](enroll-autopilot.md)

::: zone-end

::: zone pivot="ios"

- [Enroll with Company Portal](enroll-ios-company-portal.md)
- [Enroll devices with Automated Device Enrollment](enroll-ios-ade.md)
- [Enroll devices with Apple Configurator](enroll-ios-apple-configurator.md)

::: zone-end

> [!TIP]
>
> See [Plan enrollment](enrollment-planning.md) for a comparison between the enrollment methods which describes the ideal scenarios for using either option. It's recommended to review the table when planning your enrollment and deployment strategies.
