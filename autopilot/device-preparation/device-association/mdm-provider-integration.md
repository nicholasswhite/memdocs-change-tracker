---
title: Integrate an MDM provider with Windows Autopilot device association
description: Learn how a mobile device management provider can request limited access to integrate its service with Windows
  Autopilot device association.
ms.date: '2026-10-16T00:00:00Z'
author: lenewsad
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4b132a0c-342a-42eb-91ff-8159e1ed413d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/57eae307-c3a1-4cac-b645-1a899934bac8
manager: laurawi
moniker_range_name: ''
ms.author: lanewsad
ms.reviewer: madakeva
ms.service: windows-client
ms.subservice: autopilot
ms.suite: ems
ms.topic: how-to
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/ee561821-1ac7-45a8-9409-6ba5eb7a5b97
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/f2b71146-ce8e-46a8-9965-8aa8b3aa8235
---

# Integrate an MDM provider with Windows Autopilot device association

Windows Autopilot device association can support integration with a mobile device management (MDM) provider other than Microsoft Intune. Provider integration is available through a limited-access onboarding process. Microsoft must authorize the Microsoft Entra application that the provider uses before the application can access the device association service.

> [!IMPORTANT]
>
> This process is for MDM providers that are building device association into their service. It doesn't provide an individual customer or administrator with direct access to the device association service.

## Prerequisites

Before requesting access, the MDM provider should:

- Support Windows device enrollment and management by using the Windows MDM protocols. For more information, see [Mobile Device Management overview](https://learn.microsoft.com/en-us/windows/client-management/mdm-overview).
- Integrate its MDM service with Microsoft Entra ID. For more information, see [Microsoft Entra integration with MDM](https://learn.microsoft.com/en-us/windows/client-management/azure-active-directory-integration-with-mdm).
- Register the Microsoft Entra application that the service uses to call device association APIs.
- Define how customers authorize the provider to perform device association operations for their tenant.

## Request access

Contact your Microsoft representative to request onboarding for Windows Autopilot device association. Include the following information:

- The provider's legal company name and MDM product name.
- Primary business and technical contacts.
- The Microsoft Entra tenant ID for the provider.
- The application (client) ID for each Microsoft Entra application and environment that requires access.
- A description of the device association scenarios that the integration supports.
- The expected customer scale, geographic availability, and planned release timeline.

Microsoft reviews the provider identity, application identity, and proposed use case. Microsoft might request additional technical, security, privacy, or compliance information during the review.

> [!NOTE]
>
> Submitting a request doesn't guarantee approval. Microsoft doesn't publish a fixed review timeline for limited-access onboarding.

## Complete technical onboarding

If the request is approved, Microsoft:

1. Authorizes the approved Microsoft Entra application identity to use the device association service.
2. Provides the provider with the applicable API, permission, and validation requirements.
3. Defines the testing and production-readiness steps that must be completed before the integration is made available to customers.

Access is associated with the approved application identity and use case. It isn't transferable to another application or product. Contact Microsoft before changing an approved application ID, adding an environment, or materially changing the integration scenario.

## Provider responsibilities

An approved MDM provider is responsible for:

- Using device association access only for the approved MDM integration and scenarios.
- Ensuring that each customer authorizes the provider to perform device association operations for the customer's tenant.
- Requesting only the permissions required for the integration.
- Protecting credentials and device, tenant, and association data.
- Maintaining audit records for device association operations.
- Providing customer support for the provider's implementation.
- Notifying Microsoft about security incidents, ownership changes, or changes to the approved application identity or use case.

## Related content

- [Overview of Windows Autopilot device association](overview.md)
- [Requirements for Windows Autopilot device association](requirements.md)
- [Device association lifecycle management](lifecycle-management.md)
