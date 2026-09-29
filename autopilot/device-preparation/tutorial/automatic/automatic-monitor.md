---
title: "Windows Autopilot device preparation in automatic mode for Windows 365: Monitor the Windows Autopilot device preparation in automatic mode for Windows 365 deployment"
description: How to - Windows Autopilot device preparation in automatic mode for Windows 365 - Step 6 of 6 - Monitor the deployment.
ms.date: "2025-06-11T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
---

# Windows Autopilot device preparation in automatic mode for Windows 365: Monitor the Windows Autopilot device preparation in automatic mode for Windows 365 deployment

Windows Autopilot device preparation in automatic mode for Windows 365 steps:

- Step 1: [Set up Windows automatic Intune enrollment](automatic-automatic-enrollment.md)
- Step 2: [Create an assigned device group](automatic-device-group.md)
- Step 3: [Assign applications and PowerShell scripts to device group](automatic-assign-apps-scripts.md)
- Step 4: [Create Windows Autopilot device preparation policy](automatic-autopilot-policy.md)
- Step 5: [Create a Cloud PC provisioning policy](automatic-cloud-pc-provisioning-policy.md)

- **Step 6: Monitor the deployment**

For an overview of the Windows Autopilot device preparation in automatic mode for Windows 365 workflow, see [Windows Autopilot device preparation in automatic mode for Windows 365 overview](automatic-workflow.md#workflow).

## Monitor the deployment

With other Windows Autopilot and Windows Autopilot device preparation scenarios, deployments can be "viewed" on actual devices to see the deployment progress and result. However, with Windows Autopilot device preparation in automatic mode for Windows 365, the setup and deployment of the Cloud PC takes place in the background where it can't be viewed. Deployments can instead be monitored through the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) including [Windows Autopilot device preparation reporting and monitoring](../../reporting-monitoring.md).

### View status of the deployment

To view status of a Windows Autopilot device preparation in automatic mode for Windows 365 deployment:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left hand pane.
3. In the **Devices | Overview** screen, under **Device onboarding**, select **Windows 365**.
4. At the top of the **Devices | Windows 365** screen, select **All Cloud PCs**.
5. The status of each Cloud PC is displayed under the **Status** column in this page. The statuses include:

   - **Provisioning** - the Cloud PC is being provisioned and isn't ready for use yet.
   - **Preparing** - the Cloud PC is undergoing Windows Autopilot device preparation configuration and isn't ready for use yet.
   - **Provisioned** - the Cloud PC is successfully provisioned and is ready to be used.
   - **Failed** - the Cloud PC failed to be provisioned successfully and can't be used due to the setting **Prevent users from connection to Cloud PC upon installation failure or timeout** option enabled in the Cloud PC provisioning policy. For more information, see [Create a Cloud PC provisioning policy for use with Windows Autopilot device preparation in automatic mode for Windows 365](automatic-cloud-pc-provisioning-policy.md#create-a-cloud-pc-provisioning-policy-for-use-with-windows-autopilot-device-preparation-in-automatic-mode-for-windows-365).
   - **Provisioned with warnings** - the Cloud PC failed to be provisioned successfully but can be used due to the setting **Prevent users from connection to Cloud PC upon installation failure or timeout** option not being enabled in the Cloud PC provisioning policy. For more information, see [Create a Cloud PC provisioning policy for use with Windows Autopilot device preparation in automatic mode for Windows 365](automatic-cloud-pc-provisioning-policy.md#create-a-cloud-pc-provisioning-policy-for-use-with-windows-autopilot-device-preparation-in-automatic-mode-for-windows-365).

   > [!TIP]
   >
   > The Cloud PCs can be filtered based on the different statuses by selecting the appropriate status above the table.

### View granular status of the deployment

To view granular status of the Windows Autopilot device preparation in automatic mode for Windows 365 deployment, including status of individual apps and scripts, use [Windows Autopilot device preparation reporting and monitoring](../../reporting-monitoring.md):

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left hand pane.
3. In the **Devices | Overview** screen, select **Monitor**.
4. In the **Devices | Monitor** screen, in the list of reports under **Report name**, select **Windows Autopilot device preparation deployments**.
5. The **Device enrollment - Autopilot deployments** screen opens. In the **Device enrollment - Autopilot deployments** screen, deployments of individual devices is shown. Each device has the following information:

   - **Device name** - The name given to the device during the deployment. Selecting this item goes to the deployment details for the device.
   - **Enrollment date** - The date and time that the device enrolled.
   - **Deployment status** - Displays the current status of the deployment on the device. During deployment, the status shows **In progress**. Once deployment is complete, it shows the final outcome of the deployment as either **Success** or **Failed**.
   - **Phase** - Shows the last reported phase that the deployment is at. Options include:
     - **Policy installation** - Represents the initial setup and line-of-business apps installation.
     - **Script installation** - Tracks scripts.
     - **App installation** - Tracks Win32 and Microsoft Store apps.
   - **Serial number** - The hardware serial number of the device.
   - **Deployment time** - The amount of time that the deployment took during the out-of-box experience (OOBE) to complete. If the deployment isn't complete, it shows **In progress**.
   - **UPN** - The user that signed in to the device during OOBE and that the Windows Autopilot device preparation policy was assigned to.
6. Select an individual device under **Device name**. The **Device deployment details** pane opens. The **Device deployment details** pane contains three sections:

   1. **Device** - Contains information regarding the device, including:

      - **Device name** - The name given to the device during the deployment. Selecting this item goes to the device details in Intune.
      - **Deployment status** - Displays the current status of the deployment on the device. During deployment, the status shows **In progress**. Once deployment is complete, it shows the final outcome of the deployment as either **Success** or **Failed**.
      - **Device ID** - The device ID of the device in Intune.
      - **Microsoft Entra device ID** - The device ID of the device in Microsoft Entra ID.
      - **Serial number** - The hardware serial number of the device.
      - **Deployment policy** - The Windows Autopilot device preparation policy the device received.
      - **Policy Version** - The version of the Windows Autopilot device preparation policy the device received. The version number increments by one each time a change is made and saved to the Windows Autopilot device preparation policy.
      - **OS version** - The version of Windows installed on the device during the deployment.
   2. **Apps** - Reflects the last reported status for the applications being installed during the Windows Autopilot device preparation including the list of applications being installed. Statuses include:

      - **Installed** - Application was successfully installed.
      - **In progress** - Application is currently being installed.
      - **Skipped** - Usually indicates that the application was selected in the Windows Autopilot device preparation policy, but wasn't assigned to the device group specified in the Windows Autopilot device preparation policy. It can also mean that the application isn't applicable to the device.
      - **Failed** - The application failed to install. Check logs for further details.

      > [!NOTE]
      >
      > A [known issue](../../known-issues.md#win32-winget-and-enterprise-app-catalog-applications-are-skipped-when-managed-installer-policy-is-enabled-for-the-tenant) causes Win32, Microsoft Store, and Enterprise app catalog apps to be skipped when a managed installer is configured.
   3. **Scripts** - Contains information regarding the PowerShell scripts being run during the Windows Autopilot device preparation including the list of scripts being run. Statuses include:

      - **Installed** - The PowerShell script successfully ran.
      - **In progress** - The PowerShell script is currently running.
      - **Skipped** - Usually indicates that the PowerShell script was selected in the Windows Autopilot device preparation policy, but wasn't assigned to the device group specified in the Windows Autopilot device preparation policy.
      - **Failed** - The PowerShell script failed to run. Check logs for further details.

> [!IMPORTANT]
>
> Windows 365 devices that are reprovisioned after a failed deployment will not be deleted from Intune and will remain in the Autopilot device preparation report to allow for you to download the diagnostic logs when an error occurs. To clean up the stale records, use [Intune cleanup rules](../../../../intune/governance/configure-cleanup-rules.md) or delete manually.
