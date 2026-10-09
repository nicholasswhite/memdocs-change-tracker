---
title: "Device action: new Remote Assistance session"
description: Learn how to use the new remote assistance session action in Intune to offer support to your users.
ms.date: "2025-10-27T00:00:00Z"
ms.topic: how-to
author: paolomatarazzo
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/63959238-cb90-4871-a33d-4a5519097e47
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.author: paoloma
ms.collection: M365-identity-device-management
ms.reviewer: mattcall
ms.service: microsoft-intune
ms.subservice: remote-actions
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/78d87f42-5582-4a6b-90be-7db2f12b34e6
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Device action: new Remote Assistance session

Microsoft Intune provides remote assistance capabilities to help IT support teams troubleshoot and resolve issues on user devices. This functionality is available through two integration paths: **Remote Help** (part of the Intune Suite) and **TeamViewer**. Each option offers different features, licensing requirements, and setup steps.

## How It Works

When selecting the **New remote assistance session** action in Intune:

- If your tenant is configured for **Remote Help**, the session will launch using Microsoft's Remote Help app.
- If your tenant is configured for **TeamViewer**, the session will launch using TeamViewer's remote support interface.

## Learn More

Every solution has its own requirements and options. For more information, see:

- [Use Remote Help with Microsoft Intune](../../remote-help/index.md)
- [Use TeamViewer to remotely administer Intune devices](../tools/teamviewer-legacy.md)
