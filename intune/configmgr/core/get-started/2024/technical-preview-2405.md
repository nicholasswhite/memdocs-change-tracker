---
title: "Features in Configuration Manager technical preview version 2405"
description: Learn about new features available in the Configuration Manager technical preview branch version 2405.
ms.date: "2024-06-07T00:00:00Z"
ms.topic: whats-new
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: tier3
---

# Features in Configuration Manager technical preview version 2405

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2405. Install this version to update and add new features to your technical preview site. When you install a new technical preview site, this release is also available as a baseline version.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Configuration Manager now supports SQL Extended Protection for Authentication

Configuration Manager now supports SQL Extended Protection for Authentication. It's a security feature that enhances protection against MITM attacks, making SQL Server more secure when connections are made using Extended Protection. These enhancements collectively reduce the risk of unauthorized access and protect sensitive data managed by the SQL Server Database Engine.

For more information, see [Connect to the Database Engine Using Extended Protection](https://learn.microsoft.com/en-us/sql/database-engine/configure-windows/connect-to-the-database-engine-using-extended-protection)

## BitLocker support in Arm devices

Configuration Manager now supports BitLocker Task Sequence steps for Arm devices. In BitLocker Management, policies that include OS Drive encryption with a TPM protector and Fixed Drive encryption with the Auto-Unlock option are supported on Arm devices.

## Performance Enhancement of policy processing and collection evaluation

The performance of policy processing and collection evaluation has been enhanced. Previously, blocking chains from sp_ProcessPolicyChanges, called by PolicyPv, would run for hours, disrupting multiple workloads including collection management and policy processing.

## Introducing Centralized Search - Desired Workspace Selection

The centralized search box now enables the option to select the desired workspace for searching. Users can easily refine their search results by selecting the desired workspace from the dropdown menu.

[![Screenshot of centralized search workspace selection in console.](media/27679763-search-workspace.png)](media/27679763-search-workspace.png#lightbox)

## Known issues

### Unable to import or connect to Powershell Configuration Manager module via console

While importing or connecting to Configuration manager Powershell module via CM console users get the following error message : `PS C:\Build\AdminConsole\bin> Import-Module .\ConfigurationManager.psd1 Import-Module : The module manifest 'C:\Build\AdminConsole\bin\ConfigurationManager.psd1' could not be processed because it is not a valid Windows PowerShell restricted language file. Remove the elements that are not permitted by the restricted language`

### Configuration Manager console won't automatically update

If you update a technical preview site from version 2401 to a later version, the Configuration Manager console fails to update. This problem is because of a known issue in the extension installer.

**Mitigation:** To work around this issue, after you update the site from version 2401 to a later version, manually uninstall the previous console and run **ConsoleSetup.exe**.

For more information, see [Install the Configuration Manager console](../../servers/deploy/install/install-consoles.md)

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
