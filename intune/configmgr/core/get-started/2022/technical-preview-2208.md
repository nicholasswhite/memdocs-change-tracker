---
title: "Features in Configuration Manager technical preview version 2208"
description: Learn about new features available in the Configuration Manager technical preview branch version 2208.
ms.date: "2022-08-29T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Features in Configuration Manager technical preview version 2208

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2208. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Intune role-based access control (RBAC) for tenant attached devices

You can now use Intune role-based access control (RBAC) when interacting with tenant attached devices from the Microsoft Intune admin center. For example, when using Intune as the role-based access control authority, a user with Intune's [Help Desk Operator role](../../../../fundamentals/role-based-access-control/overview.md#built-in-roles) doesn't need an assigned security role or additional permissions from Configuration Manager. For more information, see [Intune role-based access control for tenant attached clients.](../../../cloud-attach/use-intune-rbac.md)

## Dark theme is now extended to more dashboards

In this release, the dark theme has been extended to more dashboards, which previously didn't display the dark theme correctly. For example, the Office 365 Updates Dashboard, PCM Dashboard, and Health Attestation dashboard will now display according to the dark theme, when it's enabled.

Enable this prerelease feature to experience the dark theme. For more information, see [Dark theme for the console.](../../servers/manage/admin-console.md)

## Issues that are fixed

If the osdinjection.xml file is directly modified, it isn't correctly preserved updating to a new Configuration Manager version. Example modifications include adding support for more binaries or for an alternate content provider (ACP). When this issue occurs, operating system deployment task sequences fail to resolve required dependencies. The smsts.log file contains the following error.

`Failed to load TSCore.dll Code (0x8007007E).`

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
