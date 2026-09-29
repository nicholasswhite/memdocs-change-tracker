---
title: "Enable local Windows Autopilot Reset"
description: Local Windows Autopilot Reset in Intune.
ms.date: "2025-04-01T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Enable local Windows Autopilot Reset

To enable a local Windows Autopilot Reset, the **DisableAutomaticReDeploymentCredentials** policy must be configured. This policy is documented in the [Policy CSP](https://learn.microsoft.com/en-us/windows/client-management/mdm/policy-csp-credentialproviders#disableautomaticredeploymentcredentials). By default, local Windows Autopilot Reset is disabled. This default ensures that a local Windows Autopilot Reset isn't accidentally triggered.

## Workflow

The following steps are required to enable and trigger local Windows Autopilot Reset:

1. Create a configuration profile in Intune that enables local Windows Autopilot Reset.
2. Make sure WinRE is installed on device where Windows Autopilot Reset is triggered.
3. Trigger Windows Autopilot Reset locally on device with an account that has local administrator privileges.

## Enable local Windows Autopilot Reset in Intune

To create a configuration profile that sets the **DisableAutomaticReDeploymentCredentials** policy and enables local Windows Autopilot Reset in Intune, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left pane.
3. In the **Devices | Overview** screen, expand **Manage devices**, and then select **Configuration**.
4. In the **Devices | Configuration** screen:

   1. At the top, make sure **Policies** is selected.
   2. Select the **Create** drop down menu and then select **New Policy**.
5. In the **Create a profile** window that opens:

   1. Under **Platform**, select **Windows 10 and later**.
   2. Under **Profile type**, select **Templates**.
   3. When the templates appear, under **Template name**, select **Device restrictions**. If **Device restrictions** isn't visible, scroll through the **Template name** list until **Device restrictions** is visible or search for **Device restrictions** in the **Search by profile name** box.
   4. Select **Create** to close the **Create a profile** window.
6. In the **Device restrictions** screen that opens:

   1. In the **Basics** page:

      1. Next to **Name**, enter a name for the domain join profile.
      2. Next to **Description**, enter a description for the domain join profile.
      3. Select **Next**.
   2. In the **Configuration settings** page:

      1. Scroll through the list and locate **General**.
      2. Select **General** to expand it.
      3. Under **General**, scroll down and locate **Autopilot Reset**.
      4. Next to **Autopilot Reset**, select **Allow**.
      5. select **Next**.
7. In the **Assignments** page:

   1. Under **Included groups**, select **Add groups**.

      > [!NOTE]
      >
      > Make sure to add the correct device groups under **Included groups** and not under **Excluded groups**. Accidentally adding the desired device groups under **Excluded groups** results in those devices being excluded and they don't receive the Windows Autopilot profile.
   2. In the **Select groups to include** window that opens, select the groups that the configuration profile should be assigned to and then select **Select**. The device groups selected here are normally the same device groups created when implementing the different [Windows Autopilot scenarios](../autopilot-scenarios.md).
   3. Under **Included groups** &gt; **Groups**, ensure the correct groups are selected, and then select **Next**.
8. In the **Applicability Rules** page, select **Next**. For this tutorial, applicability rules are being skipped. However if applicability rules are needed, do so at this screen. For more information about scope tags, see [Applicability rules](../../../intune/device-configuration/create-device-profile.md#applicability-rules).
9. In the **Review + Create** page, review and verify that all of the settings are set as desired, and then select **Create** to create the domain join profile.

## Trigger local Windows Autopilot Reset

To trigger a local Windows Autopilot Reset on a device, follow these steps:

1. Make sure that the [Windows Recovery Environment (WinRE)](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference) is correctly configured and enabled on the device where the Windows Autopilot Reset is being performed. WinRE can be enabled with the [REAgentC.exe tool](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/reagentc-command-line-options) via the following command:

   ```cmd
   reagentc.exe /enable
   ```
2. Make sure that the device is in the device group where the Windows Autopilot Reset configuration profile was assigned to.
3. If a provisioning package was created that should be applied during the local Windows Autopilot Reset, plug in the USB drive that contains the provisioning package.
4. From the Windows device lock screen, enter the keystroke `CTRL` + `WIN` + `R`.
5. To trigger the local Windows Autopilot Reset, sign in to the device with an account that has local administrator credentials.

Once the local Windows Autopilot Reset is triggered, the reset process starts. Once provisioning is complete, the device is again ready for use.

## Related content

For more information on local Windows Autopilot Reset, see the following articles:

- [Reset devices with local Windows Autopilot Reset](../../windows-autopilot-reset.md#reset-devices-with-local-windows-autopilot-reset).
- [Windows Recovery Environment (WinRE)](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference).
- [REAgentC.exe tool](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/reagentc-command-line-options).
