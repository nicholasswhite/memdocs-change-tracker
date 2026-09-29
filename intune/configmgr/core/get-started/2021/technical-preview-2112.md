---
title: "Features in Configuration Manager technical preview version 2112"
description: Learn about new features available in the Configuration Manager technical preview branch version 2112.
ms.date: "2021-12-10T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 2112

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2112. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Customize maximum run time for other software update types

Previously, software updates that didn't belong to the following update categories defaulted to a [maximum run time](../../../sum/plan-design/plan-for-software-updates.md#bkmk_maxruntime) of 60 minutes (or 10 minutes prior to version 2103):

- Windows feature updates
- Windows non-feature updates
- Office 365 updates

Starting in this technical preview, you can customize the maximum run time for all other software updates, which includes third-party updates.

### Try it out!

Try to complete the tasks. Then send [Feedback](../../understand/product-feedback.md) with your thoughts on the feature.

Change the maximum run time for all other software updates:

1. Go to **Administration** &gt; **Overview** &gt; **Site Configuration** &gt; **Sites** then select the top-level site.
2. From the ribbon, select **Settings** &gt; **Configure Site Components** &gt; **Software Update Point** to open the **Software Update Point Component Properties**.
3. In the **Maximum Run Time** tab, change the following property to a value between 5 and 9999:

   **Maximum run time for all other software updates outside these categories, such as third-party updates (minutes)**

> [!NOTE]
>
> The new run time for these updates only applies to updates that are newly synchronized after the change. Existing updates that have already been synchronized will not use this value.

## Console and user experience improvements

Based on your feedback, we’ve made a few improvements to the console and user experience.

- When using temporary device nodes, right-click device actions like **Run Scripts** are now available to make the experience in the console consistent
  - For example, if you're in the **Client Health Dashboard** then select a specific version from the **Client Versions** chart, you're taken to a temporary node. The temporary node now has additional actions available from the right-click menu
- Copy/paste is available for more objects from details panes.
  - Added the **Name** property in the details pane for configuration items, configuration item related policies, and applications
- Company portal no longer displays an available package as a featured application
- Software update search results and the search criteria are now cached when you navigate to another node. When you navigate back to the **All Software Updates** node, your search criteria and results are preserved from your last query.

## Exclude data warehouse reporting tables from synchronization

When you install the [data warehouse](../../servers/manage/data-warehouse.md), it synchronizes a set of default tables from the site database. These tables are required for data warehouse reports. While troubleshooting issues, you may want to stop synchronizing these default tables. Starting in this release, you can exclude one or more of these required tables from synchronization.

### Try it out!

Try to complete the tasks. Then send [Feedback](../../understand/product-feedback.md) with your thoughts on the feature.

1. When you install or configure the properties of the data warehouse, on the **Synchronization settings** page, choose **Select tables**.
2. In the **Database tables** window, deselect one or more tables of type **Required**.
3. The console will prompt you to confirm the change, since some reports may no longer work correctly.

## A new remote assistance tool

As announced at Microsoft Ignite 2021, a public preview of the new remote assistance solution is now available in the Microsoft Intune admin center. This cloud-based tool can help you more securely support users of Windows devices.

This new tool will be the solution for remote control of remote devices. While you can't currently start this tool from the Configuration Manager console, [tenant attach](https://learn.microsoft.com/en-us/intune/configmgr/tenant-attach/device-sync-actions?toc=/mem/configmgr/cloud-attach/toc.json&bc=/mem/configmgr/cloud-attach/breadcrumb/toc.json) provides the mechanism to eventually provide these Remote Help capabilities.

With the release of this new tool, the Configuration Manager feature for remote control anywhere using cloud management gateway (CMG) won't be available in the next technical preview release.

For more information, see the following resources:

- [Remote Help: a new remote assistance tool from Microsoft (blog post)](https://techcommunity.microsoft.com/t5/microsoft-endpoint-manager-blog/remote-help-a-new-remote-assistance-tool-from-microsoft/ba-p/2822622)
- [Enable remote help scenarios with Microsoft Intune (demo video)](https://techcommunity.microsoft.com/t5/video-hub/enable-remote-help-scenarios-with-microsoft-endpoint-manager/ba-p/2911349)
- [Use Remote Help with Intune and Configuration Manager](../../../../remote-help/index.md)

## General known issues

### Unable to install an existing console extensions after site upgrade

After a site upgrade, console extensions that aren't built into Configuration Manager won't install for new consoles. If the extension was already installed on a console, that console may continue to use the extension.

#### Workaround

To work around this issue, [delete the extension](../../servers/manage/admin-console-extensions.md#about-the-console-extensions-node) from the **Console Extensions** node. Redownload the extension from Community hub or reimport the extension and enable notifications for it as needed.

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
