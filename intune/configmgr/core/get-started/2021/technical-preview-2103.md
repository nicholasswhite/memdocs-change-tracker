---
title: "Features in Configuration Manager technical preview version 2103"
description: Learn about new features available in the Configuration Manager technical preview branch version 2103.
ms.date: "2021-03-03T00:00:00Z"
ms.subservice: core-infra
ms.topic: whats-new
ROBOTS: NOINDEX
ms.collection: tier3
ms.service: configuration-manager
---

# Features in Configuration Manager technical preview version 2103

*Applies to: Configuration Manager (technical preview branch)*

This article introduces the features that are available in the technical preview for Configuration Manager, version 2103. Install this version to update and add new features to your technical preview site. When you install a new technical preview site, this release is also available as a baseline version.

Review the [technical preview](../technical-preview.md) article before installing this update. That article familiarizes you with the general requirements and limitations for using a technical preview, how to update between versions, and how to provide feedback.

The following sections describe the new features to try out in this version:

## Community hub support for configuration baselines

Community hub now supports contributing and downloading [configuration baselines](../../../compliance/deploy-use/create-configuration-baselines.md) including the child configuration items. This integration allows administrators to easily share and reuse configuration baselines and configuration items. Baselines with software updates or version-specific references aren't supported. Contributing and downloading configuration baselines is also available for current branch versions of Configuration Manager. For more information, see [What's new in community hub](../../servers/manage/community-hub.md#bkmk_new) and [Contribute to the community hub](../../servers/manage/community-hub-contribute.md).

![Configuration baseline in community hub](media/7983121-configuration-baseline.png)

### Contributing a configuration baseline

When you contribute a configuration baseline, each of the child configuration items is verified. The verification starts at the lowest nested level. This means that configuration items that are grandchildren are verified before direct child configuration items are. The following process occurs to ensure the configuration baseline is usable and complete:

1. Check if the child configuration item is already in the community hub. If the configuration item doesn't exist, it's created.
   - A configuration item with software updates or version-specific references will cause an error and the contribution will fail.
2. If the configuration item already exists in the community hub, verify the contributor is the author. If the contributor isn't the author, a new configuration item is created in community hub.
3. If the contributor is the author, check for local updates to the configuration item. If the configuration item changed, update the item in the community hub.

## Tenant attach: Antivirus policy supports exclusions merge

When a tenant attached device is targeted with two or more [antivirus policies](../../../tenant-attach/deploy-antivirus-policy.md), the settings for antivirus exclusions will merge before being applied to the client. This change results in the client receiving the exclusions defined in each policy, allowing for more granular control of antivirus exclusions.

### Try it out!

Try to complete the tasks. Then send [Feedback](../../understand/find-help.md#product-feedback) with your thoughts on the feature.

#### Prerequisites

- All of the prerequisites for [Tenant attach: Create and deploy endpoint security policies from the admin center](../../../tenant-attach/deploy-antivirus-policy.md).
- The latest version of the Configuration Manager client installed

#### Create two policies with different antivirus exclusions

1. Create an antivirus policy from the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) that includes some [antivirus exclusions](https://learn.microsoft.com/en-us/intune/device-configuration/endpoint-security/ref-antivirus-defender-settings-windows-tenant-attach?toc=/mem/configmgr/tenant-attach/toc.json&bc=/mem/configmgr/tenant-attach/breadcrumb/toc.json#microsoft-defender-antivirus-exclusions).
2. Create a second antivirus policy including only antivirus exclusions that are different from the first policy.
3. [Assign both antivirus policies](../../../tenant-attach/deploy-antivirus-policy.md#bkmk_av) to the same collection.
4. Observe the results on a client in the targeted collection. Antivirus exclusions from both policies are applied.

## Cloud attach during site upgrade

The Microsoft Intune family of products is an integrated solution for managing all of your devices. Cloud attach brings together Configuration Manager and Intune into a single console called Microsoft Intune admin center. If you haven't already enabled the following cloud attach features, now the site upgrade process lets you cloud attach the site:

- [Co-management](../../../comanage/index.yml)
- [Tenant attach](../../../tenant-attach/index.yml)
- [Endpoint analytics](../../../../endpoint-analytics/index.md)

### Prerequisites for cloud attach during upgrade

The same prerequisites apply as for tenant attach. For more information, see [Enable tenant attach](../../../tenant-attach/device-sync-actions.md).

The new pages in the Updates Wizard only appear when you update the site from technical preview branch version 2102 or later.

### Try it out!

Try to complete the tasks. Then send [Feedback](https://learn.microsoft.com/en-us/configmgr/core/understand/find-help#product-feedback) with your thoughts on the feature.

1. Install the update for 2103 technical preview branch. For more information, see [Install in-console updates](../../servers/manage/install-in-console-updates.md).
2. On the new **Cloud attach** page of the Updates Wizard, select **Sign in**. Sign in to Microsoft Entra ID with a *Global Administrator* account.

   The wizard enables the following options by default:

   - **Enable Microsoft Intune admin center**
   - **Enable automatic client enrollment for co-management**

   By default, Configuration Manager uses your Global Administrator credentials to register an app in your Microsoft Entra tenant. It uses this app to authorize synchronization of data between your on-premises site and Intune. To use an app that you already created, select **Optionally import a separate web app...**.

   > [!IMPORTANT]
   >
   > The [Microsoft Entra Global Administrator](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/privileged-roles-permissions) role is a highly privileged role and should only be used when another role can't be used. This feature requires the Global Administrator role. For other features, Microsoft recommends using roles with the fewest permissions. To learn more, see [Fundamentals of role-based administration for Configuration Manager](../../understand/fundamentals-of-role-based-administration.md).
3. On the **Configure upload** page of the wizard, select the recommended device upload setting of **All my devices managed by Microsoft Endpoint Configuration Manager**. If needed, you can limit upload to a single device collection.

   The wizard enables by default the option to **Enable Endpoint analytics for devices uploaded to Microsoft Endpoint Manager**. Use Endpoint Analytics to get insights to optimize the end-user experience. For more information, see [Endpoint Analytics Overview](../../../../endpoint-analytics/index.md)
4. On the **Enablement** page of the wizard, configure automatic device enrollment to Intune.
5. On the **Workloads** page, configure which device authority manages each supported workload. For more information, see [How to switch Configuration Manager workloads to Intune](../../../comanage/how-to-switch-workloads.md).
6. If you configure a workload for Pilot Intune, use the **Staging** page of the wizard to select a device collection for the pilot.
7. Complete the Updates Wizard.

After the site finishes updating to version 2103, you can take advantage of the cloud attach features.

To help troubleshoot, use the following log files:

- For upgrade progress, see **ConfigMgrSetup.log** at the root of the system drive.
- For more information on cloud attach, see **CMGatewaySyncUploadWorker.log** in the site's log directory.

### Known issue with cloud attach during site upgrade

If you opt out of cloud attach during the Updates Wizard, you still need to sign in on the **Cloud attach** page. It doesn't enable cloud attach features if you don't select them, but you can't continue the wizard unless you authenticate.

## New CMG deployments use TLS 1.2

Starting in this release, new deployments of the cloud management gateway (CMG) by default enable the option to **Enforce TLS 1.2**. This change doesn't affect existing deployments. While not recommended, if you need to use the less secure TLS protocol versions, you can still disable this option.

For more information, see the following articles:

- [Cloud management gateway overview](../../clients/manage/cmg/overview.md)
- [How to enable TLS 1.2](../../plan-design/security/enable-tls-1-2.md)

## PowerShell release notes preview

These release notes summarize changes to the Configuration Manager PowerShell cmdlets in technical preview version 2103.

For more information about PowerShell for Configuration Manager, see [Get started with Configuration Manager cmdlets](https://learn.microsoft.com/en-us/powershell/sccm/overview).

### New cmdlets

#### Remove-CMClientSettingDeployment

Use this cmdlet to remove a specific deployment of a client setting.

```powershell
$clientSettingId = (Get-CMClientSetting -name "Remote control").SettingsID

Remove-CMClientSettingDeployment -CollectionID 'XYZ0003F' -ClientSettingsID $clientSettingId
```

### Modified cmdlets

#### Fast support

The following cmdlets now support the **Fast** parameter. Use this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause more network traffic and affect cmdlet performance.

- Get-CMAlert
- Get-CMAlertSubscription
- Get-CMBaseline
- Get-CMBaselineDeployment
- Get-CMBaselineDeploymentStatus
- Get-CMClientCertificatePfx
- Get-CMComplianceRule
- Get-CMComplianceSetting
- Get-CMConfigurationPlatform
- Get-CMConfigurationPolicyDeployment
- Get-CMDriver
- Get-CMDriverPackage
- Get-CMTaskSequence
- Get-CMTaskSequenceDeployment

#### Get-CMPackage

**Non-breaking changes**

Added parameter "PackageType" for retrieving specific package type.

## Next steps

For more information about installing or updating the technical preview branch, see [Technical preview](../technical-preview.md).

For more information about the different branches of Configuration Manager, see [Which branch of Configuration Manager should I use?](../../understand/which-branch-should-i-use.md).
