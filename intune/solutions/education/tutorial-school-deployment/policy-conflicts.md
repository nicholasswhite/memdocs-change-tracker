---
title: "Avoiding policy conflicts"
description: Learn how to avoid policy conflicts when creating and deploying new policies.
ms.date: "2024-07-11T00:00:00Z"
ms.topic: tutorial
---

# Avoiding policy conflicts

![](../../../media/icons/16/check.svg) Ensure policies apply effectively to devices

Devices and users targeted with the same setting from different policies cause conflicts. When conflicts occur, Intune generates an error and doesn't apply either setting. As a result, it's important to avoid or resolve conflicts to ensure the correct configuration is applied. Use the steps in this document when creating new policies to avoid or resolve policy conflicts.

> [!NOTE]
>
> If you only use Intune for Education to manage your devices, you can easily update the settings or apps that you have deployed to existing groups or create new groups to apply new policies or apps. You don't need to do anything extra to prevent conflicts if the members of the new groups are different from the members of the existing groups.

## 1. Determine which users or devices need the new policy

Review the existing Microsoft Entra ID groups and determine if they're applicable for the new policy. Otherwise, create a new group and add users or devices.

## 2. Identify and review potentials sources of conflict

The key to avoiding policy conflicts is to understand if existing policies targeted at the same set of users or devices contain the same settings. If a new policy has settings that overlap with existing ones for the same users or devices, either exclude those users or devices from the old policies or remove the overlapping settings.

You can exclude groups of devices or users using the "exclude group" option or by excluding devices using [filters](../../../fundamentals/filters/overview.md).

> [!TIP]
>
> For more information about grouping and targeting, see [Plan Education device grouping and targeting](grouping-and-targeting.md).

### Default policies for Education tenants

When Intune licenses are added to an Education tenant for the first time, a set of default policies are created. These policies can be viewed in the Configuration policies list in the Intune admin center. They should be reviewed for overlapping settings to determine if exclusions are required when targeting the same set of users or devices. By default, these policies are targeted to *All Devices*.

Default policy names:

- **Devices** &gt; **Windows** &gt; **Configuration**
  - Default Policies for EDU
  - Default Admx policy for EDU
  - Edition Upgrade
  - Shared PC Policy
- **Devices** &gt; **Windows** &gt; **Windows updates** &gt; **Update rings**
  - Windows Update Policy

> [!NOTE]
>
> If you're using Intune for Education, you can see and change these settings by navigating to **Groups** and then selecting the group **All Devices** or **All Users** &gt; **Settings**. Select **Windows device settings** or **iOS device settings**.

### Policies created in the Intune for Education console

When you configure settings in Intune for Education, corresponding policies are created in the Intune service that can be viewed and edited from the Intune admin console. Configuration profiles created by Intune for Education have a recognizable naming template that always starts with the name of the group followed by a suffix based on the template type. The *&lt;GROUP NAME&gt;* part of each name represents the group that was selected in Intune for Education when the settings were configured.

This list provides examples of configuration profiles created by Intune for Education. They should be reviewed for overlapping settings to determine if exclusions are required when targeting the same set of users or devices.

- **Devices** &gt; **Windows** &gt; **Configuration**
  - *&lt;GROUP NAME&gt;* Windows10General
  - *&lt;GROUP NAME&gt;* GroupPolicyConfiguration
  - *&lt;GROUP NAME&gt;* Windows10EndpointProtection
  - *&lt;GROUP NAME&gt;* Windows10CustomDenyAdministrativeApps
  - *&lt;GROUP NAME&gt;* Windows10CustomDenyStore
  - *&lt;GROUP NAME&gt;* Windows10SharedPC
  - *&lt;GROUP NAME&gt;* Windows10EnterpriseModernAppManagement
  - *&lt;GROUP NAME&gt;* ConfigurationPolicy
- **Devices** &gt; **Windows** &gt; **Enrollment** &gt; **Windows Autopilot/Deployment Profiles**
  - *&lt;GROUP NAME&gt;* Windows10AutopilotProfile
- **Devices** &gt; **Windows** &gt; **Windows updates** &gt; **Update rings**
  - *&lt;GROUP NAME&gt;* Windows10UpdatesForBusiness
- **Devices** &gt; **Windows** &gt; **Windows updates** &gt; **Feature Updates**
  - *&lt;GROUP NAME&gt;* WindowsFeatureUpdates
- **Endpoint security** &gt; **Account protection**
  - *&lt;GROUP NAME&gt;*_LocalUsersAndGroupsConfig_EDU

## 3. Assign the policy to target group

Once all the potential sources of conflict are reviewed and any exclusions are configured, you can assign the new policy to the user or device groups. Assign the policy using "Included groups" and optionally use assignment filters.

## 4. Monitoring for policy conflicts

- [![](../../../media/icons/16/intune.svg) Intune](#tabpanel_1_intune)
- [![](../../../media/icons/16/intune.svg) Intune for Education](#tabpanel_1_intune-for-education)

<a id="tabpanel_1_intune"></a>



You can check for potential policy conflicts by going to **Devices** &gt; **Monitor** &gt; **Configuration policy assignment failure**. Find the new policy and review any conflicts in the report. The report can also be exported to CSV.

<a id="tabpanel_1_intune-for-education"></a>



You can check for potential policy conflicts by going to **Reports** &gt; **Settings error**.

If a conflict is found, remove the overlapping settings from the new policy or exclude the targeted users or devices from existing policies.
