---
title: "Features in Configuration Manager technical preview version 1907"
description: Learn about new features available in the Configuration Manager technical preview branch version 1907.
ms.date: "2019-07-11T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ROBOTS: NOINDEX
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 1907

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 1907. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Search the task sequence editor

If you have a large task sequence with many groups and steps, it can be difficult to find specific steps. Based on your feedback, you can now search in the task sequence editor. This action lets you more quickly locate steps in the task sequence.

![Searching in the task sequence editor](media/4621085-task-sequence-search.png)

Search using the following criteria:

- Step name
- Step type
- Step description
- Group name
- Variable name
- Conditions
- Other content, for example, strings like variable values or command lines

You can also filter for all steps with the following attributes:

- Continue on error
- Has conditions

When you search, the editor window highlights in yellow the steps that match your search criteria.

You can quickly access these search fields and navigate the search results with the following keyboard shortcuts:

- **CTRL** + **F**: enter a search string
- **CTRL** + **O**: select the search options to scope the results
- **F3** or **Enter**: step forward through the results
- **SHIFT** + **F3**: step backwards through the results

## Improvements to Office 365 ProPlus upgrade readiness dashboard

We've made improvements to the **Office 365 ProPlus upgrade readiness** dashboard that released in [Technical Preview version 1904](technical-preview-1904.md#bkmk_o365). The following new tiles on this dashboard help you evaluate readiness:

- Deployment
- Macro advisories
- Top add-ins by count of version

In the Configuration Manager console, go to the **Software Library** workspace, expand **Office 365 Client Management**, and select the **Office 365 ProPlus Upgrade Readiness** node.

![Office 365 ProPlus upgrade readiness dashboard](media/4021125-office-365-upgrade-readiness-dashboard.png)

![Office 365 ProPlus upgrade readiness dashboard - add-ins](media/4021125-office-365-to-add-ins.png)

![Office 365 ProPlus upgrade readiness dashboard - macro advisories](media/4021125-office-365-macro-advisories.png)

For more information on prerequisites and using this data, see [Integration for Microsoft 365 Apps readiness](https://learn.microsoft.com/en-us/sccm/sum/deploy-use/office-365-dashboard#bkmk_o365_readiness).

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md)
