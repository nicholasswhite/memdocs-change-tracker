---
title: "Reseller, distributor, or partner registration"
description: Windows Autopilot device registration by CSP partners lets resellers and distributors add customer devices through
  Partner Center.
ms.date: '2026-10-30T00:00:00Z'
ms.topic: how-to
ms.collection:
  - M365-modern-desktop
  - m365initiative-coredeploy
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
  - ✅ <a href="https://learn.microsoft.com/hololens/hololens-release-notes" target="_blank">Windows Holographic</a>
ms.custom: sfi-ga-nochange
author: iceorbital
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4b132a0c-342a-42eb-91ff-8159e1ed413d
moniker_range_name: ''
ms.author: acabello
ms.reviewer: madakeva
ms.service: windows-client
ms.subservice: autopilot
ms.suite: ems
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/f2b71146-ce8e-46a8-9965-8aa8b3aa8235
---

# Reseller, distributor, or partner registration

Customers can purchase devices from resellers, distributors, or other partners. If these resellers, distributors, and partners are part of the [Cloud Solution Partners (CSP) program](https://partner.microsoft.com/cloud-solution-provider), they can register devices for the customer.

As with manufacturers, CSP partners must be granted permission to register devices for an organization. This process is described in the [CSP authorization](registration-auth.md#csp-authorization) section of the Windows Autopilot customer consent article. In summary:

- The CSP partner requests a relationship with the organization. That organization's Global Administrator approves the request.
- After the approval, CSP partners add devices by using [Partner Center](https://partner.microsoft.com/pcv/dashboard/overview), either directly through the website or by using available APIs that can automate the same tasks.

For Surface devices, Microsoft Support can help with device registration. For more information, see [Surface Registration Support for Windows Autopilot](https://learn.microsoft.com/en-us/surface/surface-autopilot-registration-support).

Windows Autopilot doesn't require delegated administrator permissions when it establishes the relationship between the CSP partner and the organization. As part of the Global Administrator's approval process, they can choose to unselect **Include delegated administration permissions**.

> [!IMPORTANT]
>
> The [Microsoft Entra Global Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/privileged-roles-permissions) role is a highly privileged role that should only be used when another role can't be used. This feature requires the Global Administrator role. For other features, Microsoft recommends using roles with the fewest permissions.

> [!TIP]
>
> While resellers, distributors, or partners could boot each new Windows device to get the hardware hash so they can provide it to customers or register the device directly, we don't recommend this method. Instead, register devices by using the PKID information from the device packaging, such as the barcode, or get it electronically from the manufacturer or upstream partner or distributor.

> [!NOTE]
>
> Partner Center doesn't have access to profiles you create in Intune or Microsoft Store for Business. It only has access to the Windows Autopilot profiles you create through Partner Center.

## Related content

- [Registration overview](registration-overview.md)
