---
title: Become a Microsoft Intune Mobile Device Management Partner
description: Learn the eligibility criteria and application process for becoming a Microsoft Intune mobile device management
  (MDM) compliance partner.
ms.date: '2026-11-03T00:00:00Z'
ai-usage: ai-assisted
author: ilwu-microsoft
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/57eae307-c3a1-4cac-b645-1a899934bac8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
moniker_range_name: ''
ms.author: ilwu
ms.collection:
- M365-identity-device-management
- compliance
- sub-device-compliance
ms.reviewer: ilwu-microsoft
ms.service: microsoft-intune
ms.subservice: protect
ms.topic: how-to
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/ee561821-1ac7-45a8-9409-6ba5eb7a5b97
---

# Become a Microsoft Intune Mobile Device Management Partner

The Third-Party Compliance MDM Partner Program is designed for mobile device management (MDM) solutions that determine and manage compliance for user-associated devices and use Microsoft Entra ID to communicate device compliance status to Microsoft services.

## Supported scenarios

To be eligible as an Intune compliance partner, your MDM solution must meet the following criteria:

- Manage devices using MDM protocols.
- Evaluate device compliance for user-based scenarios.
- Use Microsoft Entra ID for user identification.
- Support one or more of the following platforms: Android, iOS/iPadOS, and macOS.

## Apply to become an Intune compliance MDM partner

Partners interested in integrating with Microsoft should begin by creating a Microsoft Entra app for their MDM product. For instructions, see [Register a Microsoft Entra app and create a service principal](https://learn.microsoft.com/en-us/entra/identity-platform/howto-create-service-principal-portal).

After you create a Microsoft Entra app and obtain a Microsoft Entra app ID, you can apply to become a partner through the [Intune Compliance MDM Partner Application](https://forms.cloud.microsoft/r/GKYuFnrSdv).

Microsoft uses the submitted information to validate that:

- The solution aligns with the intended Intune and Microsoft Entra ID Conditional Access scenario.
- The proposed integration is appropriate for the Intune Device Compliance API.
- The partner is prepared to provide enterprise-grade support to customers after launch.

To protect your organization and customers, do not include detailed implementation information, source code, API payloads, security internals, proprietary design details, or other information not reasonably necessary for Microsoft's evaluation.

Microsoft reviews partner applications in the order they are received. Review timelines may vary based on application volume and team capacity. Applicants should generally allow several weeks for an initial response. Once an application has been reviewed, Microsoft will contact the business or technical contacts listed in the application with follow-up questions or information outlining next steps. Please note that submission of an application does not guarantee approval to integrate, inclusion in a public listing, or production availability. Microsoft may also request additional information during the review process.

Partners are responsible for implementing the integration based on the provided documentation. Microsoft does not guarantee dedicated onboarding assistance, implementation guidance, or engineering support during development.

Submission of an application does not guarantee API documentation access, approval to integrate, public listing, or production availability. Microsoft might request additional information as part of the review process.

Microsoft may change the structure, organization, or presentation of its documentation at any time. Participation in the program does not guarantee that Microsoft will feature, promote, or otherwise provide marketing visibility for a partner or its solution.

> [!NOTE]
>
> For partners onboarded through the new self-service process, Microsoft does not publish partner-specific setup documentation or list each partner by name in the Microsoft Intune admin center. Partners should provide their customers with the setup information required to use their solution.

To configure an MDM integration, a customer adds a custom MDM compliance partner in the Intune admin center by entering the Microsoft Entra application ID provided by their selected third-party MDM provider. Intune uses this application ID to create the connector and enable the partner integration.
