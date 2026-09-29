---
title: "Features in Configuration Manager technical preview version 2107"
description: Learn about new features available in the Configuration Manager technical preview branch version 2107.
ms.date: "2021-07-29T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ROBOTS: NOINDEX
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 2107

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2107. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Tenant attach: Software updates information

There's a new **Software updates** page for tenant attached devices. This page displays the status for software updates on a device. You can review which updates are successfully installed, failed, and are assigned but not yet installed. Using the timestamp for the update status assists with troubleshooting.

The following actions are available on the **Software update** page for a tenant attached device:

- **Search**: You can search using either a full or partial string in all columns except **Status time**.
- **Sort**: Sort a column by using the arrows after the column name. The default sort order is by **Status time**.
- **Refresh**: Retrieves updated information for the device from the Configuration Manager environment.
- **Export**: Exports all of the available data for the device to a `.csv` file.

[![Screenshot of the software updates page for a tenant attached device](media/6024419-software-updates.png)](media/6024419-software-updates.png#lightbox)

## Publish query to Community hub from CMPivot

You can now publish a CMPivot query to the Community hub directly from the CMPivot window. Submitting your queries directly through CMPivot makes contributing to the Community hub easier.

### Prerequisites:

- Meet all of the [CMPivot prerequisites and permissions](../../servers/manage/cmpivot.md#prerequisites)
- Enable [Community hub](../../servers/manage/community-hub.md).
  - If needed, install the Microsoft Edge WebView2 extension from the [Configuration Manager console notification](../../servers/manage/community-hub.md#bkmk_webview2).
- A GitHub account that's [joined to Community hub](../../servers/manage/community-hub-contribute.md#join-the-community-hub-to-contribute-content)
  - You must accept the invitation sent in the email otherwise you won't be able to contribute content.

#### Use CMPivot to publish a query to the Community hub

1. Go to the **Assets and Compliance** workspace then select the **Device Collections** node.
2. Select a target collection, target device, or group of devices then select **Start CMPivot** in the ribbon to launch the tool.
3. From the CMPivot window, select the Community hub icon on the menu.

   ![Community hub icon](../../servers/manage/media/7137169-hub-icon.png)
4. Select **Sign in**, then sign in to GitHub.
5. Create a [query](../../servers/manage/cmpivot-overview.md), then select **Run Query** to verify it functions as expected.

   - Optionally, select the folder icon to access your favorites list to use a query you've already created.
6. Select the **Publish** link at top of CMPivot's Community hub window when you're ready to submit your query.  ![Screenshot of the Community hub window in CMPivot showing the publishing tab](media/9965423-publish.png)
7. Give your query a **Name** and **Description**, then select the **Publish** button to send your query to the Community hub.
8. Once the contribution is complete, you can access your query anytime from the **Me** tab.
9. To view the GitHub pull request (PR), go to <https://github.com/Microsoft/configmgr-hub/pulls>. You can also access the PR link from the **Your hub** page in the **Community hub** node.

   - PRs shouldn't be submitted directly to the GitHub repository.

> [!NOTE]
>
> Community hub is only available in CMPivot when you run it from the Configuration Manager console. Community hub isn't available from [standalone CMPivot](../../servers/manage/cmpivot.md#install-cmpivot-standalone).

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
