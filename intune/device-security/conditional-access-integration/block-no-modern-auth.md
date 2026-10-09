---
title: "Block Apps That Don't Use Modern Authentication (MSAL)"
description: Learn about applications and modern authentication (MSAL) using Microsoft Intune.
ms.date: "2024-03-28T00:00:00Z"
author: lenewsad
ms.author: lanewsad
ms.topic: article
ms.reviewer: beflamm
ms.collection:
- M365-identity-device-management
- sub-device-compliance
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/1e31b9be-b6e9-4221-a20b-d1460dbd5dfa
- https://authoring-docs-microsoft.poolparty.biz/devrel/5f286262-a4cb-47f4-92d3-dc24f172492b
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
manager: laurawi
moniker_range_name: ''
ms.service: microsoft-intune
ms.subservice: protect
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/8d63a4c4-4889-43b4-a98e-8e50dbfdb083
- https://authoring-docs-microsoft.poolparty.biz/devrel/90571f66-8410-4272-8117-79ce87fc2dcc
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
---

# Block Apps That Don't Use Modern Authentication (MSAL)

App-based Conditional Access with app protection policies rely on applications using [modern authentication](https://support.office.com/article/Using-Office-365-modern-authentication-with-Office-clients-776c0036-66fd-41cb-8928-5495c0f9168a), which is an implementation of OAuth2. Most current Office mobile and desktop applications use modern authentication. However, there are third-party apps and older Office apps that use other authentication methods, like basic authentication and forms-based authentication.

## Block access to apps

To block access to apps that don't use modern authentication, use Intune app protection policies to implement Conditional Access. For more information, see [App-based Conditional Access with Intune](app-based-policies.md).

## Additional information

For more information about Microsoft Entra Conditional Access, see the following topics:

- [What is Conditional Access in Microsoft Entra ID?](https://learn.microsoft.com/en-us/entra/identity/conditional-access/overview)
- [How app-based Conditional Access works](app-based-policies.md#how-app-based-conditional-access-works)

## Next steps

- [App-based Conditional Access with Intune](app-based-policies.md)
