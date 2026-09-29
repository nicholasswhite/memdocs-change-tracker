---
title: "Features in Configuration Manager technical preview version 2203"
description: Learn about new features available in the Configuration Manager technical preview branch version 2203.
ms.date: "2022-03-02T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 2203

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2203. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Dark theme for the console

The Configuration Manager console now offers a dark theme. To use the theme, select the arrow from the top left of the ribbon, then choose **Switch console theme**. Select **Switch console theme** again to return to the light theme. Using a console theme can help you easily distinguish a test environment from a production environment or one hierarchy from another.

The console dark theme is a [pre-release](../../servers/manage/pre-release-features.md) feature. Currently, there are certain locations in the console that may not display the dark theme correctly.

![Screenshot of the Configuration Manager using the dark theme for the console. The 'Switch console theme' option is displayed in the upper right corner of the image.](media/9070525-console-dark-theme.png)

### Known issue

When you first switch to a different theme, you may notice the node navigation pane doesn't properly render when you move to a new workspace. To work around this issue, restart the console.

## Escrow BitLocker recovery password to the site during a task sequence

You can now configure the **Enable BitLocker** step of a task sequence to escrow the BitLocker recovery information for the OS volume to Configuration Manager. Previously, you had to escrow to Active Directory, or wait for the Configuration Manager client to receive BitLocker management policy after the task sequence. This new option makes sure that the device is fully protected by BitLocker when the task sequence completes, and that you can recover the OS volume immediately.

For more general information, see [Plan for BitLocker management](../../../protect/plan-design/bitlocker-management.md).

### Prerequisites for escrowing BitLocker recovery password during a task sequence

The client will only escrow its key to the Configuration Manager site if you configure one of the following options:

- Create and use a certificate to encrypt the site database for BitLocker management.
- Enable the BitLocker client management policy option to **Allow recovery information to be stored in plain text**.

For more information, see [Encrypt recovery data in the database](../../../protect/deploy-use/bitlocker/encrypt-recovery-data.md).

### Try it out!

Try to complete the tasks. Then send [Feedback](../../understand/product-feedback.md) with your thoughts on the feature.

1. If needed, first [create a task sequence to deploy an OS](../../../osd/deploy-use/manage-task-sequences-to-automate-tasks.md).
2. [Use the task sequence editor](../../../osd/understand/task-sequence-editor.md) to edit the task sequence.
3. If the task sequence doesn't already include the **Enable BitLocker** step, add it. For more information, see [About task sequence steps: Enable BitLocker](../../../osd/understand/task-sequence-steps.md#enable-bitlocker).
4. On the properties of the **Enable BitLocker** step, select the option to **Automatically store the recovery key**, and then select **The Configuration Manager database**.

   > [!NOTE]
   >
   > If Configuration Manager can't escrow the key, by default this task sequence step fails.

## PowerShell release notes preview

These release notes summarize changes to the Configuration Manager PowerShell cmdlets in this technical preview release.

For more information about PowerShell for Configuration Manager, see [Get started with Configuration Manager cmdlets](https://learn.microsoft.com/en-us/powershell/sccm/overview).

### Module changes

The following folder-related cmdlets now support software update groups and deployment packages:

- [Get-CMFolder](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/get-cmfolder)
- [New-CMFolder](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/new-cmfolder)
- [Remove-CMFolder](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/remove-cmfolder)
- [Set-CMFolder](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/set-cmfolder)
- [Move-CMObject](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/move-cmobject)
- [Add-CMObjectSecurityScope](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/Add-CMObjectSecurityScope)
- [Remove-CMObjectSecurityScope](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/Remove-CMObjectSecurityScope)

For more general information, see [Added folder support for nodes in the Software Library](technical-preview-2202.md#bkmk_folder).

### Modified cmdlets

#### New-CMSoftwareUpdateDeployment

For more information, see [New-CMSoftwareUpdateDeployment](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/New-CMSoftwareUpdateDeployment).

**Non-breaking changes**

Added parameter **PreDownloadUpdateContent** to support [pre-download for available software updates](technical-preview-2202.md#bkmk_pre-download).

#### Set-CMSoftwareUpdateDeployment

For more information, see [Set-CMSoftwareUpdateDeployment](https://learn.microsoft.com/en-us/powershell/module/configurationmanager/Set-CMSoftwareUpdateDeployment).

**Non-breaking changes**

Added parameter **PreDownloadUpdateContent** to support [pre-download for available software updates](technical-preview-2202.md#bkmk_pre-download).

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
