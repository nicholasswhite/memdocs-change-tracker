---
title: "Reset devices with remote Windows Autopilot Reset"
description: Remote Windows Autopilot Reset in Intune.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Reset devices with remote Windows Autopilot Reset

Intune can be used to start the remote Windows Autopilot Reset process. Resetting in this way avoids the need for someone to visit each device that needs to be reset to start the Windows Autopilot Reset process. Unlike [local Windows Autopilot reset](local-autopilot-reset.md), a configuration profile doesn't need to be configured or assigned for remote Windows Autopilot Reset to work. Remote Windows Autopilot Reset is available on any Microsoft Entra join device that is a Windows Autopilot device without any additional configuration.

## Workflow

The following steps are required to enable and trigger local Windows Autopilot Reset:

1. Make sure WinRE is installed on device where Windows Autopilot Reset is triggered.
2. Make sure Intune admin has appropriate privileges in Intune to perform remote Windows Autopilot Resets.
3. In Intune, remotely trigger Windows Autopilot Reset on device.
4. Force device to start the remote Windows Autopilot Reset (optional).

## Triggering a remote Windows Autopilot Reset

To trigger a remote Windows Autopilot Reset via Intune, follow these steps:

1. Make sure that the [Windows Recovery Environment (WinRE)](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference) is correctly configured and enabled on the device where the Windows Autopilot Reset is being performed. WinRE can be enabled with the [REAgentC.exe tool](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/reagentc-command-line-options) via the following command:

   ```cmd
   reagentc.exe /enable
   ```
2. Make sure the Intune admin initiating the remote Windows Autopilot Reset is a member of the Intune Service Administrator role. For more information, see [Add users and grant administrative permission to Intune](../../../intune/fundamentals/tenant-administration/add-users.md).
3. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
4. In the **Home** screen, select **Devices** in the left pane.
5. In the **Devices | Overview** screen, under **By platform**, select **Windows**.
6. In the **Windows | Windows devices** screen, under **Device name** select the targeted devices to perform the Windows Autopilot Reset.
7. In the page that opens that displays the properties of the device, select **Autopilot Reset** in the toolbar at the top of the window.
8. A Windows Autopilot Reset warning message is displayed. Select **Yes** to continue.
9. A message should display confirming that the Windows Autopilot reset is initiated. The Windows Autopilot Reset should start shortly thereafter on the device.

Once the Windows Autopilot Reset is complete, the device is again ready for use.

## Forcing a device to start the remote Windows Autopilot Reset

Unlike [local Windows Autopilot reset](local-autopilot-reset.md), when the remote Windows Autopilot Reset is initiated for a device, the reset might not start immediately. Instead, the reset will occur when the device next checks in with Intune and gets updated policy. For more information, see [Policy refresh intervals](../../../intune/device-configuration/troubleshoot-device-profiles.md#policy-refresh-intervals)

A Windows Autopilot Reset can be forced to start sooner on a device by forcing the device to obtain the latest Intune policy. Forcing remote Windows Autopilot Reset to start sooner can be done either remotely or locally on the device.

### Remotely force a device to start the remote Windows Autopilot Reset

To force the device to obtain the latest Intune policy remotely, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left pane.
3. In the **Devices | Overview** screen, under **By platform**, select **Windows**.
4. In the **Windows | Windows devices** screen, under **Device name** select the devices where the remote Windows Autopilot Reset was initiated.
5. In the page that opens that displays the properties of the device, select **Sync** in the toolbar at the top of the window.
6. A Sync warning message is displayed. Select **Yes** to continue.

These steps should force the device to obtain the latest Intune policy. The Windows Autopilot Reset should start shortly thereafter.

### Locally force a device to start the remote Windows Autopilot Reset

To force the device to obtain the latest Intune policy locally on the device, sign in to the device where the remote Windows Autopilot Reset was initiated. Once signed in to the device, open the **Accounts** &gt; **Access work or school** pane in the **Settings** app by selecting the following link:

[Access work or school](ms-settings:workplace)

Or

1. Right-click on the **Start** menu and select **Run**.
2. In the **Run** window, next to **Open:**, enter:

   ```console
   ms-settings:workplace
   ```

   and then select **OK**.

Or

1. Right-click on the **Start** menu and select **Settings**.
2. In the **Settings** app:

   - Windows 11

     1. Select **Accounts** in the left hand pane.
     2. In the **Accounts** page, select **Access work or school**.
   - Windows 10

     1. Select **Accounts**.
     2. In the left hand pane, select **Access work or school**.

Once the **Access work or school** pane is open in the **Settings** app, follow these steps:

1. In the **Accounts &gt; Access work or school** pane, select **Connected by &lt;user@domain&gt;** to expand the section.
2. In the expanded section, next to **Managed by &lt;organization&gt;**, select the **Info** button.
3. In the **Accounts &gt; Access work or school &gt; Managed by &lt;organization&gt;** page, under **Device sync status**, select the **Sync** button.

These steps should force the device to obtain the latest Intune policy. The Windows Autopilot Reset should start shortly thereafter.

## Related content

For more information on local Windows Autopilot Reset, see the following articles:

- [Reset devices with remote Windows Autopilot Reset](../../windows-autopilot-reset.md#reset-devices-with-remote-windows-autopilot-reset).
- [Windows Recovery Environment (WinRE)](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference).
- [REAgentC.exe tool](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/reagentc-command-line-options).
- [Add users and grant administrative permission to Intune](../../../intune/fundamentals/tenant-administration/add-users.md).
- [Policy refresh intervals](../../../intune/device-configuration/troubleshoot-device-profiles.md#policy-refresh-intervals).
