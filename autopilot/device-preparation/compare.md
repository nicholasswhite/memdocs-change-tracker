---
title: Compare Windows Autopilot device preparation and Windows Autopilot
description: Compare Windows Autopilot device preparation and Windows Autopilot features and when to use each.
ms.date: "2026-08-07T00:00:00Z"
ms.topic: overview
ms.collection:
  - M365-modern-desktop
  - m365initiative-coredeploy
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
---

# Compare Windows Autopilot device preparation and Windows Autopilot

## Windows Autopilot device preparation vs. Windows Autopilot

| Feature | **Windows Autopilot device preparation** | **Windows Autopilot** |
| --- | --- | --- |
| Features | - Support for Government Community Cloud High (GCCH) and Department of Defense (DoD) environments. - Faster, more consistent provisioning experience. - Near real-time monitoring and troubleshooting info. | - Support for multiple device types ([HoloLens](https://learn.microsoft.com/en-us/hololens/hololens2-autopilot), [Teams Meeting Room](https://learn.microsoft.com/en-us/microsoftteams/rooms/autopilot-autologin)). - Many customization options for the provisioning experience. |
| Supported modes | - [User-driven](tutorial/user-driven/entra-join-workflow.md). - Automatic. | - [User-driven](../tutorial/user-driven/azure-ad-join-workflow.md). - [Pre-provisioned](../tutorial/pre-provisioning/azure-ad-join-workflow.md). - [Self-deploying](../tutorial/self-deploying/self-deploying-workflow.md). - [Existing devices](../tutorial/existing-devices/existing-devices-workflow.md). |
| Join types supported | - Microsoft Entra join. | - Microsoft Entra join. - Microsoft Entra hybrid join. |
| Device registration required? | No. | Yes. |
| Is it possible to bind devices to my tenant before enrollment? | Yes, you can [associate devices](tutorial/user-driven/entra-join-device-association.md). | Yes, you can [register devices](../registration-overview.md). |
| What do admins need to configure? | - Windows Autopilot device preparation policy. - Device security group with **Intune Provisioning Client** as owner. | - Windows Autopilot deployment profile. - Enrollment Status Page (ESP). |
| What configurations can be delivered during provisioning? | - Device-based only during the out-of-box experience (OOBE). - Up to 25 essential applications (line-of-business (LOB), Win32, Microsoft Store, Microsoft 365). - Up to 10 essential PowerShell scripts. | - Device-based during device ESP. - User-based during user ESP. - Up to [100 applications](https://learn.microsoft.com/en-us/intune/intune-service/enrollment/windows-enrollment-status#block-access-to-a-device-until-a-specific-application-is-installed). |
| Reporting &amp; troubleshooting | Windows Autopilot device preparation deployment report:  - Shows all Windows Autopilot device preparation deployments. - More data available. - Near real-time. | Windows Autopilot deployment report:  - Only shows Windows Autopilot registered devices. - Not real-time. |
| Supports LOB and Win32 applications in same deployment? | Yes. | No. |
| Supported versions of Windows | - Windows 11, version 24H2 or later. - Windows 11, version 23H2 with [KB5035942](https://support.microsoft.com/topic/march-26-2024-kb5035942-os-builds-22621-3374-and-22631-3374-preview-3ad9affc-1a91-4fcb-8f98-1fe3be91d8df) or later. - Windows 11, version 22H2 with [KB5035942](https://support.microsoft.com/topic/march-26-2024-kb5035942-os-builds-22621-3374-and-22631-3374-preview-3ad9affc-1a91-4fcb-8f98-1fe3be91d8df) or later. | - All [currently supported](https://learn.microsoft.com/en-us/windows/release-health/supported-versions-windows-client#windows-11-supported-versions-by-servicing-option) versions of Windows 11 General Availability Channel. - All [currently supported](https://learn.microsoft.com/en-us/windows/release-health/supported-versions-windows-client#windows-10-supported-versions-by-servicing-option) versions of Windows 10 General Availability Channel. |

## Which Windows Autopilot solution to use

Which version of Windows Autopilot to use is dependent on many factors and variables, with each environment having different needs. Windows Autopilot device preparation in its initial offering isn't as feature rich as Windows Autopilot, but it does have some advantages and features not available in Windows Autopilot.

In general, the following are some of the major factors when considering between Windows Autopilot device preparation or Windows Autopilot:

| Requirement | **Windows Autopilot device preparation** | **Windows Autopilot** |
| --- | --- | --- |
| Government Community Cloud High (GCCH) and Department of Defense (DoD) environments | ✅ | ❌ |
| User-driven scenario | ✅ | ✅ |
| Pre-provisioned scenario | ❌ | ✅ |
| Self-deploying scenario | ❌ | ✅ |
| Existing devices scenario | ❌ | ✅ |
| Automatic deployment scenario | ✅ | ❌ |
| Windows Autopilot reset support | ❌ | ✅ |
| Microsoft Entra join | ✅ | ✅ |
| Microsoft Entra hybrid join | ❌ | ✅ |
| [Windows Autopilot Reset](../tutorial/reset/autopilot-reset-overview.md) | ❌ | ✅ |
| Windows 11 | ✅ | ✅ |
| Windows 10 | ❌ | ✅ |
| Deploy Win32 and LOB applications in the same deployment | ✅ | ❌ |
| Simpler deployment configuration and experience | ✅ | ❌ |
| Extensive customization of deployment and OOBE experience | ❌ | ✅ |
| No requirement to pre-stage devices | ✅ | ❌ |
| Install more than 10 applications during OOBE | ❌ | ✅ |
| Run more than 10 PowerShell scripts during OOBE | ❌ | ✅ |
| Near real-time monitoring | ✅ | ❌ |
| Block user from accessing desktop until user based configurations are applied | ❌ | ✅ |
| [HoloLens](https://learn.microsoft.com/en-us/hololens/hololens2-autopilot) support | ❌ | ✅ |
| [Teams Meeting Room](https://learn.microsoft.com/en-us/microsoftteams/rooms/autopilot-autologin) support | ❌ | ✅ |
| Device Firmware Configuration Interface ([DFCI](../dfci-management.md)) Management support | ❌ | ✅ |
| [Windows Autopilot into co-management](../../intune/configmgr/comanage/autopilot-enrollment.md) | ❌ | ✅ |

## Using Windows Autopilot device preparation and Windows Autopilot concurrently

Windows Autopilot device preparation and Windows Autopilot can be used concurrently and side by side within an organization. However, any one device in an environment can only run one of the two solutions. For a device that's registered with Windows Autopilot, which deployment runs depends on the device's association state. If the device isn't associated with the tenant, the Windows Autopilot profile takes precedence. If the device is associated, device association takes precedence and the Windows Autopilot device preparation deployment runs. To use Windows Autopilot device preparation on a registered device without associating it, first [deregister the device](../registration-overview.md#deregister-a-device).
