---
title: "Features in Configuration Manager technical preview version 2007"
description: Learn about new features available in the Configuration Manager technical preview branch version 2007.
ms.date: "2020-07-27T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ROBOTS: NOINDEX
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 2007

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2007. Install this version to update and add new features to your technical preview site.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Tenant attach: View hardware inventory in Microsoft Intune admin center

Hardware inventory can now be viewed for a tenant attached Configuration Manager device in the admin center.

### Try it out!

Try to complete the tasks. Then send [Feedback](technical-preview-2003.md#bkmk_feedback) with your thoughts on the feature.

#### Prerequisites

- An environment that's [tenant attached with uploaded devices](../../../tenant-attach/device-sync-actions.md).
- One of the following browsers:
  - Microsoft Edge, version 77 and later
  - Google Chrome
- The user account has been discovered with both [Microsoft Entra user discovery](../../servers/deploy/configure/about-discovery-methods.md#azureaddisc) and [Active Directory user discovery](../../servers/deploy/configure/about-discovery-methods.md#bkmk_aboutUser).
  - Meaning the user account needs to be a synced user object in Azure.

#### Permissions

The user account needs the following permissions:

- The **Admin User** role for the Configuration Manager Microservice application in Microsoft Entra ID.
  - Add the role in Microsoft Entra ID from **Enterprise applications** &gt; **Configuration Manager Microservice** &gt; **Users and groups** &gt; **Add user**. Groups are supported if you have Microsoft Entra ID P1 or P2.

#### View hardware inventory

1. In the Configuration Manager console, go to the **Assets and Compliance** workspace and select the **Devices** node.
2. Right-click on a device that's been uploaded to Microsoft Intune.
3. In the right-click menu, select **Start** &gt; **Admin Center Preview** to open the preview in your browser.
   - This launch is a preview experience. The final location will be in Microsoft Intune admin center.
4. Select **Resource Explorer** to view the hardware inventory.
   - Classes with large amounts of data will only return the first 50 entries.

## Improvements to client data sources dashboard

The [client data sources dashboard](../../servers/deploy/configure/monitor-content-you-have-distributed.md#client-data-sources-dashboard) now offers an expanded selection of filters to view information about where clients get content. These new filters include:

- Single boundary group
- All boundary groups
- Internet clients
- Clients not associated with a boundary group

In the Configuration Manager console, go to the **Monitoring** workspace, expand **Distribution Status**, and select the **Client Data Sources** node. By default, the dashboard displays information for a single boundary group. Select another option to update the dashboard. If there's no data available for the selected client group, the chart displays "This data is not yet available."

The dashboard also includes a new tile for **Content downloads using fallback source**. This information helps you understand how often clients download content from an alternate source.

[![Client data sources dashboard](media/7102084-client-data-sources.png)](media/7102084-client-data-sources.png#lightbox)

## Fixed-width font now used in some console areas

Based on your feedback, various areas in the Configuration Manager console now use the fixed-width font Consolas. This font provides consistent spacing and makes it easier to read. In this release, you'll see the Consolas font in the following places:

- Application scripts
- Configuration item scripts
- WMI-based collection membership queries
- CMPivot queries
- Scripts
- Run PowerShell Script
- Run Command Line

If there are other console areas that should use this font, send [Feedback](technical-preview-2003.md#bkmk_feedback).

[![Script editor example with fixed-width Consolas font](media/7632637-script-editor.png)](media/7632637-script-editor.png#lightbox)

## Manage task sequence policy size

Configuration Manager technical preview version 2004 included new [management insight rules for OS deployment](technical-preview-2004.md#bkmk_osdmi). These insights help you manage the policy size of task sequences. Large task sequences cause problems with client processing.

To further help manage the size of task sequences, starting in this release Configuration Manager restricts the following actions for a task sequence that's greater than 2 MB in size:

- Save changes in the task sequence editor
- Save changes with PowerShell cmdlets
- Import a new task sequence
- Any other change using supported SDK methods

For example, the task sequence editor will display an error if you try to save changes to a large task sequence.

For more information on how to remediate this issue, see [How to reduce the size of task sequence policy](technical-preview-2004.md#how-to-reduce-the-size-of-task-sequence-policy).

> [!TIP]
>
> This new behavior checks for the 2 MB size limit on the task sequence as stored in the site database. When the client processes the entire task sequence policy, the expanded size can cause problems over 32 MB. The management insights check for the 32 MB task sequence policy size.

## Improvements to device timeline in the admin center

We've added additional events to the device timeline in the admin center. You can now see the following events:

- **Event ID 20227** for **VPN failure** from the **RAS client**
- **Event ID 20009** for **MP communication roundtrip** from **Microsoft-ConfigMgr**

For more information about the device timeline, see [Configuration Manager technical preview 2005](technical-preview-2005.md#bkmk_timeline).

### Collected events for the timeline

| Event name | Provider name | Event ID | Technical preview version added |
| --- | --- | --- | --- |
| Abnormal Shutdown | Boot | 41 | 2005 |
| Application Crash | Windows Error Reporting | 1001 | 2005 |
| Application Deployment | Microsoft-ConfigMgr | 20001 | 2005 |
| Application Error | Application Error | 1000 | 2005 |
| Application Hang | Application Hang | 1002 | 2005 |
| Boundary Group Change | Microsoft-ConfigMgr | 20000 | 2005 |
| Configuration Manager – Update Installation | Microsoft-ConfigMgr | 20002 | 2005 |
| Firmware version change | Microsoft-ConfigMgr | 20003 | 2005 |
| Initiated Shutdown | Boot | 1074 | 2005 |
| Kernel Crash | Microsoft-Windows-WER-SystemErrorReporting | 1001 | 2005 |
| MP communication roundtrip | Microsoft-ConfigMgr | 20009 | 2007 |
| Unknown Shutdown | Boot | 0 | 2005 |
| VPN Failure | RASClient | 20227 | 2007 |
| Windows Update Agent – Update Installation | Microsoft-Windows-WindowsUpdateClient | 19 | 2005 |

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
