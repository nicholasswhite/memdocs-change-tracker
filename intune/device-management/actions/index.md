---
title: "Device actions"
description: Discover how to use Microsoft Intune to remotely manage, wipe, lock, restart, and secure Android, iOS/iPadOS, tvOS, visionOS, macOS, Windows, and ChromeOS devices. Learn about available device actions, prerequisites, and bulk actions for IT admins.
ms.date: "2026-09-16T00:00:00Z"
ms.topic: overview
---

# Device actions

In today's hybrid work environment, IT professionals manage and secure devices across diverse locations and platforms—often without physical access. Microsoft Intune's device actions provide a powerful toolkit to meet this challenge. These actions enable IT pros to respond quickly to incidents, enforce compliance, and maintain productivity, all from the cloud. Whether it's locking a lost device, resetting a password, or triggering a malware scan, device actions help ensure that users stay protected and supported—wherever they are.

## When device actions are useful

Device actions are especially valuable in scenarios where time and access are limited. For example:

- A device is reported lost or stolen—IT can remotely wipe or lock it to protect sensitive data.
- A device is malfunctioning—IT can restart it or run diagnostics without needing to be on-site.
- A device needs to receive a payload immediately—IT can trigger a sync to apply the latest policies.
- A malware alert is raised—security teams can initiate a Defender Antivirus scan remotely.

These capabilities reduce downtime, improve security posture, and streamline support operations.

## Prerequisites

Each action has its own prerequisites, which the respective documentation details. In general:

- Devices must be enrolled in Intune.
- Devices must be connected to the Internet to receive remote commands.
- Some actions might require specific Intune roles or permissions.

## Available device actions

Microsoft Intune supports device actions across multiple platforms. The availability of specific actions depends on the platform and the device's configuration. This cross-platform support ensures that IT pros can manage a diverse device ecosystem with consistent tools and workflows.

Select one of the following tabs to learn more about the available device actions for each platform:

- [![](../../media/icons/16/windows.svg) **Windows**](#tabpanel_1_windows)
- [![](../../media/icons/16/apple-mobile.svg) **Apple mobile**](#tabpanel_1_apple-mobile)
- [![](../../media/icons/16/macos.svg) **macOS**](#tabpanel_1_macos)
- [![](../../media/icons/16/android.svg) **Android**](#tabpanel_1_android)
- [![](../../media/icons/16/chromeos.svg) **ChromeOS**](#tabpanel_1_chromeos)

<a id="tabpanel_1_windows"></a>



| Icon | Action | Description |
| --- | --- | --- |
| ![autopilot-reset-icon](icons/autopilot-reset.svg) | [Autopilot reset](autopilot-reset.md) | Restores a device to its original settings and removes personal files, apps, and settings. |
| ![bitlocker-key-rotation-icon](icons/bitlocker-key-rotation.svg) | [BitLocker key rotation](rotate-bitlocker-keys.md) | Rotates the BitLocker recovery key for a device. |
| ![collect-diagnostics-icon](icons/collect-diagnostics.svg) | [Collect diagnostics](collect-diagnostics.md) | Collects diagnostic logs from a device and uploads the logs to Intune. |
| ![delete-icon](icons/delete.svg) | [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| ![fresh-start-icon](icons/fresh-start.svg) | [Fresh Start](fresh-start.md) | Reinstalls the latest version of Windows on a device and removes apps that the manufacturer installed. |
| ![full-scan-icon](icons/full-scan.svg) | [Full Scan](full-scan.md) | Initiates a full scan of the device by Microsoft Defender Antivirus. |
| ![locate-device-icon](icons/locate-device.svg) | [Locate device](locate.md) | Shows the approximate location of a device on a map. |
| ![pause-config-refresh-icon](icons/pause-config-refresh.svg) | [Pause Config Refresh](pause-config-refresh.md) | Pauses ConfigRefresh to run remediation on a device for troubleshooting or maintenance or to make changes. |
| ![quick-scan-icon](icons/quick-scan.svg) | [Quick Scan](quick-scan.md) | Initiates a quick scan of the device by Microsoft Defender Antivirus. |
| ![new-remote-assistance-session-icon](icons/new-remote-assistance-session.svg) | [New remote assistance session](remote-assist.md) | Allows you to remotely control a device by using [Remote Help](../../remote-help/index.md) or [TeamViewer](../tools/teamviewer-legacy.md). |
| ![restart-icon](icons/restart.svg) | [Restart](restart.md) | Restarts a device. |
| ![retire-icon](icons/retire.svg) | [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. |
| ![rotate-local-admin-password-icon](icons/rotate-local-admin-password.svg) | [Rotate Local admin password](../../device-security/laps/deploy-policy.md#manually-rotate-passwords) | Changes the local administrator password for a device and stores the password in Intune. |
| ![run-remediation-icon](icons/run-remediation.svg) | [Run remediation](run-remediation.md) | Initiates on demand Proactive Remediation |
| ![sync-icon](icons/sync.svg) | [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. |
| ![update-defender-security-intelligence-icon](icons/update-defender-intelligence.svg) | [Update Windows Defender security intelligence](https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-antivirus/manage-protection-updates-windows-defender-antivirus) | Updates the security intelligence files for Microsoft Defender Antivirus. |
| ![wipe-icon](icons/wipe.svg) | [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. |

> [!TIP]
>
> For Intel vPro devices, Intune also integrates with Intel vPro Fleet Services to provide hardware-level remote management capabilities, including out-of-band management that works even when the operating system is unresponsive or the device is powered off.

<a id="tabpanel_1_apple-mobile"></a>



| Icon | Action | Description | iOS | iPadOS | tvOS | visionOS |
| --- | --- | --- | --- | --- | --- | --- |
| ![delete-icon](icons/delete.svg) | [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |
| ![disable-activation-lock-icon](icons/disable-activation-lock.svg) | [Disable Activation Lock](disable-activation-lock.md) | Removes the Activation Lock from a device that's enrolled with a device enrollment manager (DEM) account. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![locate-device-icon](icons/locate-device.svg) | [Locate device](locate.md) | Shows the approximate location of a device on a map. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![logout-current-user-icon](icons/logout-current-user.svg) | [Logout current user](logout-user.md) | Signs out the current user from a Shared iPad. |  | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![lost-mode-icon](icons/lost-mode.svg) | [Lost mode](lost-mode.md) | Locks a device with a custom message and disables sound and vibration. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![new-remote-assistance-session-icon](icons/new-remote-assistance-session.svg) | [New remote assistance session](remote-assist.md) | Allows you to remotely control a device by using [Remote Help](../../remote-help/index.md) or [TeamViewer](../tools/teamviewer-legacy.md). | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![play-lost-mode-sound-icon](icons/play-lost-mode-sound.svg) | [Play Lost Mode sound](play-lost-mode-sound.md) | Plays Lost Mode sound on a lost device to help locate it. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![remote-lock-icon](icons/remote-lock.svg) | [Remote lock](remote-lock.md) | Locks a device and resets its password. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  | ![Supported](../../media/icons/16/check.svg) |
| ![remove-apps-and-configurations-icon](icons/remove-apps-and-configurations.svg) | [Remove apps and configurations](remove-apps-config.md) | Temporarily removes applications and configuration from a device. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![remove-user-icon](icons/remove-user.svg) | [Remove user](remove-user.md) | Deletes a user from the cache of a Shared iPad. |  | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![remove-passcode-icon](icons/remove-passcode.svg) | [Remove passcode](remove-passcode.md) | Removes the device passcode. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  | ![Supported](../../media/icons/16/check.svg) |
| ![restart-icon](icons/restart.svg) | [Restart](restart.md) | Restarts a device. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |
| ![retire-icon](icons/retire.svg) | [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |
| ![send-custom-notification-icon](icons/send-custom-notification.svg) | [Send custom notification](send-custom-notification.md) | Sends a custom notification message to a device that can be viewed in the Company Portal app. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![shut-down-icon](icons/shut-down.svg) | [Shut down](shutdown.md) | Shuts down a device. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![sync-icon](icons/sync.svg) | [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |
| ![update-cellular-data-plan-icon](icons/update-cellular-data-plan.svg) | [Update cellular data plan](update-cellular-data-plan.md) | Updates the cellular data plan settings for a device that uses an eSIM profile. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |  |  |
| ![wipe-icon](icons/wipe.svg) | [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) | ![Supported](../../media/icons/16/check.svg) |

<a id="tabpanel_1_macos"></a>



| Icon | Action | Description |
| --- | --- | --- |
| ![delete-icon](icons/delete.svg) | [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| ![disable-activation-lock-icon](icons/disable-activation-lock.svg) | [Disable Activation Lock](disable-activation-lock.md) | Removes the Activation Lock from a device that's enrolled with a device enrollment manager (DEM) account. |
| ![new-remote-assistance-session-icon](icons/new-remote-assistance-session.svg) | [New remote assistance session](remote-assist.md) | Allows you to remotely control a device by using [Remote Help](../../remote-help/index.md) or [TeamViewer](../tools/teamviewer-legacy.md). |
| ![remote-lock-icon](icons/remote-lock.svg) | [Remote lock](remote-lock.md) | Locks a device and resets its password. |
| ![restart-icon](icons/restart.svg) | [Restart](restart.md) | Restarts a device. |
| ![retire-icon](icons/retire.svg) | [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. |
| ![rotate-filevault-recovery-icon](icons/rotate-filevault-recovery.svg) | [Rotate FileVault recovery key](rotate-filevault-recovery-key.md) | Rotates the FileVault recovery key. |
| ![rotate-recovery-lock-icon](icons/rotate-recovery-lock.svg) | [Rotate Recovery Lock passcode](rotate-recovery-lock-passcode.md) | Rotates the Recovery Lock passcode. |
| ![sync-icon](icons/sync.svg) | [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. |
| ![wipe-icon](icons/wipe.svg) | [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. |

<a id="tabpanel_1_android"></a>



| Icon | Action | Description |
| --- | --- | --- |
| ![delete-icon](icons/delete.svg) | [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| ![locate-device-icon](icons/locate-device.svg) | [Locate device](locate.md) | Shows the approximate location of a device on a map. |
| ![new-remote-assistance-session-icon](icons/new-remote-assistance-session.svg) | [New remote assistance session](remote-assist.md) | Allows you to remotely control a device by using [Remote Help](../../remote-help/index.md) or [TeamViewer](../tools/teamviewer-legacy.md). |
| ![play-lost-mode-sound-icon](icons/play-lost-mode-sound.svg) | [Play lost device sound](play-lost-mode-sound.md) | Plays a sound on a lost device to help locate it. |
| ![remote-lock-icon](icons/remote-lock.svg) | [Remote lock](remote-lock.md) | Locks a device and resets its password. |
| ![remove-apps-and-configurations-icon](icons/remove-apps-and-configurations.svg) | [Remove apps and configurations](remove-apps-config.md) | Temporarily removes applications and configuration from a device. |
| ![reset-passcode-icon](icons/reset-passcode.svg) | [Reset passcode](reset-passcode.md) | Resets the device passcode. |
| ![restart-icon](icons/restart.svg) | [Restart](restart.md) | Restarts a device. |
| ![restore-managed-home-screen-icon](icons/restore-managed-home-screen.svg) | [Restore managed home screen](restore-managed-home-screen.md) | Restores the managed home screen on a device. |
| ![retire-icon](icons/retire.svg) | [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. |
| ![send-custom-notification-icon](icons/send-custom-notification.svg) | [Send custom notification](send-custom-notification.md) | Sends a custom notification message to a device that can be viewed in the Company Portal app. |
| ![suspend-managed-home-screen-icon](icons/suspend-managed-home-screen.svg) | [Suspend managed home screen](suspend-managed-home-screen.md) | Suspends the managed home screen on a device. |
| ![sync-icon](icons/sync.svg) | [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. |
| ![wipe-icon](icons/wipe.svg) | [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. |

<a id="tabpanel_1_chromeos"></a>



> [!NOTE]
>
> To manage ChromeOS devices with Intune, you must first [set up the Chrome Enterprise connector](../../device-enrollment/configure-chrome-enterprise-connector.md) and enroll devices by using the Google Admin console. This integration allows you to manage ChromeOS devices alongside other platforms in Intune.

| Icon | Action | Description |
| --- | --- | --- |
| ![retire-icon](icons/retire.svg) | [Deprovision](deprovision.md) | Removes Google Admin policies from a ChromeOS device that you no longer use. |
| ![lost-mode-icon](icons/lost-mode.svg) | [Lost mode](lost-mode.md) | Locks a lost or stolen ChromeOS device and displays a custom message and contact info configured in the Google Admin Console. In Chrome Enterprise, this action is referred to as **Disabled**. |
| ![restart-icon](icons/restart.svg) | [Restart](restart.md) | Restarts a device. |
| ![wipe-icon](icons/wipe.svg) | [Wipe](wipe.md) | Erases data from the device. You can choose to remove only user profiles or perform a full factory reset (Powerwash). A factory reset is required before re-enrollment. |

## Execute a device action from the Intune admin center

Every device action has its own steps, which the respective documentation details. In general:

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select **Devices** &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. At the top of the device overview pane, a row displays available device actions. Each icon represents a specific action (such as **Restart**, **Wipe**, or **Locate device**). Depending on your screen resolution or window size, the overflow menu (**...**) might hide some actions.
4. Select the desired action.
5. Complete any required fields, then confirm the action.

> [!NOTE]
>
> The **Retire**, **Wipe**, and **Delete** actions take precedence over all other actions. A device with multiple pending actions only carries out a Retire, Wipe, or Delete. The system ignores all other pending actions.

## Daily tenant limits

Intune limits the number of Wipe, Retire, and Delete device actions that can be submitted in a tenant each day.

| Device action | Daily limit per tenant |
| --- | --- |
| Wipe | 500 |
| Retire | 1,000 |
| Delete | 1,000 |

The limit for each action is cumulative across all submission methods, including actions for individual devices, bulk device actions, and Microsoft Graph API requests. To request a change to one of these limits, [contact Microsoft support](../../fundamentals/it-pro-support/get-support-admin-center.md).

## Check the status of the action

To check the status of the action, select **Devices** &gt; [**Device actions**](https://go.microsoft.com/fwlink/?linkid=2109431#view/#view/Microsoft_Intune_Devices/DeviceActionList.ReactView).

> [!NOTE]
>
> For **MDM devices**, deleting a device immediately hides it from the admin center and initiates a **Retire**. A status of **Completed** on a delete action means the process is complete on the server side; it doesn't confirm that the client device finished the **Retire**.

## Bulk device actions

Managing devices at scale is a common challenge for IT pros, especially in environments like schools, enterprises, or frontline operations. Microsoft Intune supports bulk device actions, so IT admins can perform tasks on up to 100 devices at the same time. This capability streamlines operations, reduces manual effort, and ensures consistent policy enforcement across large device fleets.

> [!NOTE]
>
> Bulk Wipe, Retire, and Delete requests count toward the [daily tenant limit](#daily-tenant-limits) for each action.

For example, at the end of a school year, IT admins can use bulk wipe to securely reset student devices before reassigning them for the next term. This approach saves time and ensures that sensitive data is removed efficiently across all devices.

Select one of the following tabs to learn more about the available bulk device actions for each platform:

- [![](../../media/icons/16/windows.svg) **Windows**](#tabpanel_2_windows)
- [![](../../media/icons/16/apple-mobile.svg) **Apple mobile**](#tabpanel_2_apple-mobile)
- [![](../../media/icons/16/macos.svg) **macOS**](#tabpanel_2_macos)
- [![](../../media/icons/16/android.svg) **Android**](#tabpanel_2_android)
- [![](../../media/icons/16/chromeos.svg) **ChromeOS**](#tabpanel_2_chromeos)

<a id="tabpanel_2_windows"></a>



| Bulk action | Description |
| --- | --- |
| [Autopilot reset](autopilot-reset.md) | Restores a device to its original settings and removes personal files, apps, and settings. |
| [Collect diagnostics](collect-diagnostics.md) | Collects diagnostic logs from a device and uploads the logs to Intune. |
| [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| [Rename](../inventory-and-status/rename-device.md#bulk-rename-devices) | Changes the device name in Intune. |
| [Restart](restart.md) | Restarts a device. |
| [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. |
| [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. |
| [Wipe](wipe.md) | Restores a device to the factory settings and removes all data and settings. |

<a id="tabpanel_2_apple-mobile"></a>



| Bulk action | Description |
| --- | --- |
| [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| [Rename](../inventory-and-status/rename-device.md#bulk-rename-devices) | Changes the device name in Intune. |
| [Restart](restart.md) | Restarts a device. |
| [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. |
| [Send custom notification](send-custom-notification.md) | Sends a custom notification message to a device that can be viewed in the Company Portal app. |
| [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. |
| [Update cellular data plan](update-cellular-data-plan.md) | Updates the cellular data plan settings for a device that uses an eSIM profile. |
| [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. |

<a id="tabpanel_2_macos"></a>



| Bulk action | Description |
| --- | --- |
| [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| [Rename](../inventory-and-status/rename-device.md#bulk-rename-devices) | Changes the device name in Intune. |
| [Restart](restart.md) | Restarts a device. |
| [Retire](retire.md) | Removes company data and settings from a device, and leaves personal data intact. |
| [Sync](sync.md) | Syncs a device with Intune to apply the latest policies and configurations. |
| [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. |

<a id="tabpanel_2_android"></a>



| Bulk action | Description |
| --- | --- |
| [Activate eSIM](update-cellular-data-plan.md#activate-esims-on-multiple-android-enterprise-devices) | Activates eSIMs on supported corporate-owned Android Enterprise devices. |
| [Delete](delete.md) | Removes a device from Intune management, removes any company data, and retires the device. |
| [Rename](../inventory-and-status/rename-device.md#bulk-rename-devices) | Changes the device name in Intune. |
| [Restart](restart.md) | Restarts a device. |
| [Wipe](wipe.md) | Restores a device to its factory settings and removes all data and settings. |

<a id="tabpanel_2_chromeos"></a>



| Bulk action | Description |
| --- | --- |
| [Deprovision](deprovision.md) | Removes Google Admin policies from a ChromeOS device that you no longer use. |
| [Lost mode](lost-mode.md) | Locks a lost or stolen ChromeOS device and displays a custom message and contact info configured in the Google Admin Console. In Chrome Enterprise, this action is referred to as **Disabled**. |
| [Restart](restart.md) | Restarts a device. |
| [Wipe](wipe.md) | Erases data from the device. You can choose to remove only user profiles or perform a full factory reset (Powerwash). A factory reset is required before re-enrollment. |

## Execute a bulk device action

Each bulk action has its own steps. The documentation for each action provides detailed instructions. In general, follow these steps:

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices) &gt; [**Bulk device actions**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_Devices/BulkActionWizardBlade).
2. On the **Basics** page, select an **OS** and **Device action** from the dropdowns. Some device actions have more options or fields to fill in. Select **Next**.
3. On the **Devices** page, select up to the maximum number of devices that the action supports. Select **Next**.
4. On the **Review + create** page, select **Create**.

## Next steps

Device actions in Intune empower IT pros to manage devices efficiently and securely—whether individually or at scale. Explore the documentation linked in this article to learn more about each action and how to integrate them into your device management workflows.
