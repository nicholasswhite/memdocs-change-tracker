---
title: "Known issues with deployments in Microsoft Intune (preview)"
description: "Review known issues and limitations for deployments during public preview in Microsoft Intune."
ms.date: "2026-08-26T00:00:00Z"
---

# Known issues with deployments in Microsoft Intune (preview)

> [!IMPORTANT]
>
> These known issues apply to the public preview release of deployments. This list is updated as issues are resolved or identified.

The following known issues and limitations apply to deployments during public preview:

- The Deployments page does not currently support sorting options. The list is sorted based on when a ring starts in an active deployment.
- Search in the Deployments page only searches on deployment name.
- When you create a deployment for a payload protected by a Multi Admin Approval access policy, the deployment doesn't appear in the **Deployments** list until the approval is complete.
- To view the Multi Admin Approval status for a Deployment, open the deployment or use Tenant administration: Multi Admin Approval, or Admin tasks.

## Related articles

- [Deployment plans and deployments overview](overview.md)
- [Create a deployment plan in Microsoft Intune](create-deployment-plan.md)
- [Create and manage a deployment in Microsoft Intune](create-deployment.md)
- [Permissions, scope tags, and approvals for deployments](rbac-scope-tags.md)
- [Use Multi Admin Approval in Intune](../../fundamentals/role-based-access-control/multi-admin-approval.md)
- [Public preview in Microsoft Intune](../../fundamentals/public-preview.md)
