---
title: "Pre-provision Microsoft Entra join: Technician flow"
description: How to - Windows Autopilot for pre-provisioned deployment Microsoft Entra join - Step 8 of 9 - Technician flow.
ms.date: "2025-04-09T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Pre-provision Microsoft Entra join: Technician flow

Windows Autopilot for pre-provisioned deployment Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](azure-ad-join-automatic-enrollment.md)
- Step 2: [Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)
- Step 3: [Register devices as Windows Autopilot devices](azure-ad-join-register-device.md)
- Step 4: [Create a device group](azure-ad-join-device-group.md)
- Step 5: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](azure-ad-join-esp.md)
- Step 6: [Create and assign Windows Autopilot profile](azure-ad-join-autopilot-profile.md)
- Step 7: [Assign Windows Autopilot device to a user (optional)](azure-ad-join-assign-device-to-user.md)

- **Step 8: Technician flow**

- Step 9: [User flow](azure-ad-join-user-flow.md)

For an overview of the Windows Autopilot for pre-provisioned deployment Microsoft Entra join workflow, see [Windows Autopilot for pre-provisioned deployment Microsoft Entra join overview](azure-ad-join-workflow.md#workflow).

## Technician flow

Once all of the configurations for Windows Autopilot for pre-provisioned deployment are completed in Intune and in Microsoft Entra ID, the next step is to start the Windows Autopilot deployment process on the device. For Windows Autopilot for pre-provisioned deployment, the Windows Autopilot process is split into two different phases that run at two different points in time by two different sets of individuals:

- The first phase is known as the **technician flow** and is normally run by the IT department, OEM, or reseller.
- The second phase is known as the **user flow** and is normally run by the end-user.

To start the technician flow, select a device that is part of the device group created in the previous **Create a device group** step, and then follow these steps:

1. If a wired network connection is available, connect the device to the wired network connection.
2. Power on the device.
3. Once the device boots up, one of two things occurs depending on the state of network connectivity:

   - If the device is connected to a wired network and has network connectivity, the device might reboot to apply critical security updates (if available or applicable). After the reboot to apply critical security updates, the Windows Autopilot process begins.
   - If the device isn't connected to a wired network or if it doesn't have network connectivity, it prompts to connect to a network. Connectivity to the Internet is required:

     1. The out-of-box experience (OOBE) begins and a screen asking for a country or region appears. Select the appropriate country or region, and then select **Yes**.
     2. The keyboard screen appears to select a keyboard layout. Select the appropriate keyboard layout, and then select **Yes**.
     3. An additional keyboard layouts screen appears. If needed, select additional keyboard layouts via **Add layout**, or select **Skip** if no additional keyboard layouts are needed.

        > [!NOTE]
        >
        > When there's no network connectivity, the device can't download the Windows Autopilot profile to know what country/region and keyboard settings to use. For this reason, when there's no network connectivity, the country/region and keyboard screens appear even if these screens are set to hidden in the Windows Autopilot profile. These settings need to be specified in these screens in order for the network connectivity screens that follow to work properly.
     4. The **Let's connect you to a network** screen appears. At this screen, either plug the device into a wired network (if available), or select and connect to a wireless Wi-Fi network.
     5. Once network connectivity is established, the **Next** button should become available. Select **Next**.
     6. At this point, the device might reboot to apply critical security updates (if available or applicable). After the reboot to apply critical security updates, the Windows Autopilot process begins.

4. At the Microsoft Entra sign-in page, **DON'T** sign in or select the **Next**/**Sign in** button. Instead, press the `WIN` key on the keyboard five times. Pressing the `WIN` key five times should display a **What would you like to do?** options screen instead.
5. From the **What would you like to do?** options screen:

   - For Windows 10, select the **Windows Autopilot provisioning** option, and then select **Continue**.
   - For Windows 11, select the **Pre-provision with Windows Autopilot** option, and then select **Next**.
6. In the **Windows Autopilot Configuration** screen (Windows 10) or the **Pre-provision with Windows Autopilot** screen (Windows 11), it displays the following information about the deployment:

   - The name of the organization for the device.
   - The name of the Windows Autopilot deployment profile assigned to the device during the **Create and assign Windows Autopilot profile** step.
   - The user assigned to the device if a user was assigned to the device in the **Assign Windows Autopilot device to a user (optional)** step (if applicable).
   - A QR code containing a unique identifier for the device. This code can be used to look up the device in Intune to perform actions such as verifying configurations, make any necessary changes, etc.
7. Validate that the information in the **Windows Autopilot Configuration** screen is correct. Once all information is confirmed as correct, select **Provision** (Windows 10) or **Next** (Windows 11) to begin the provisioning process.
8. The device might reboot, followed by the Enrollment Status Page (ESP) appearing. The Enrollment Status Page (ESP) displays progress during the provisioning process across three phases:

   - **Device preparation** (Device ESP)
   - **Device setup** (Device ESP)
   - **Account setup** (User ESP)

   The first two phases of **Device preparation** and **Device setup** are part of the Device ESP while the final phase of **Account setup** is part of the User ESP.

   For technician flow of the Windows Autopilot for pre-provisioned deployment, only the first two Device ESP phases of **Device preparation** and **Device setup** run. The last User ESP phase of **Account setup** will run during the next step of **User flow**.
9. Once **Device setup** and the device ESP process completes, a status screen is displayed showing whether the provisioning process either succeeded of failed:

   - If the pre-provisioning process completes successfully, a success status screen appears with information about the deployment. Information presented includes the previously presented information of organization name, Windows Autopilot deployment profile name, QR code (Windows 10 only), and if applicable, assigned user. The elapsed time of the provisioning process is also provided.

     Select **Reseal** to shut down the device. At that point, the device can be delivered to the end-user.

     > [!IMPORTANT]
     >
     > Outside of testing scenarios, if the intention is to deliver the device to an end-user, **DON'T** turn the device back on at this point. Instead, deliver the device to the end-user where they perform the last step of **User flow**.
   - If the pre-provisioning process fails, an error status screen appears with information about why the deployment failed including an error. The error screen also displays the previously presented information of organization name, Windows Autopilot deployment profile name, QR code (Windows 10 only), and if applicable, assigned user. The elapsed time of the provisioning process is also provided.

     From this screen, diagnostic logs can be gathered from the device to troubleshoot the issue by using the following methods:

     - In Windows 10, select **View diagnostics**.
     - In Windows 11, enter the keystroke `CTRL`+`SHIFT`+`D` and then select **Export Logs**.

     If the issue can be easily fixed, for example resolving network connectivity, then select the **Retry** button to retry provisioning the device. Otherwise if the issue can't be immediately fixed or can't be fixed without a reset, then select the **Reset** button so that the process starts over again.

## Technician flow tips

- Before the Windows Autopilot deployment is started, Microsoft recommends having:

  - At least one type of policy and at least one application assigned to the devices.
  - At least one type of policy and at least one application assigned to the users.

  These assignments ensure proper testing of the Windows Autopilot deployment during both the device ESP phase and user ESP phase of the ESP. It might also prevent possible issues when there are either no policies or no applications assigned to the devices or the users.

- Depending on how the Windows Autopilot profile was configured at the **Create and assign Windows Autopilot profile** step, additional screens might appear during the Windows Autopilot deployment before the Microsoft Entra sign-in page such as:  
     
  - **Language**/**Country**/**Region**.
  - **Keyboard**.
  - **License Terms**.

- To view and hide detailed progress information in the ESP during the provisioning process:  
     
  - **Windows 10**: To show details, next to the appropriate phase select **Show details**. To hide the details, next to the appropriate phase select **Hide details**.
  - **Windows 11**: To show details, next to the appropriate phase select **∨**. To hide the details, next to the appropriate phase select **∧**.

- The technician flow inherits behavior from [self-deploying mode](../self-deploying/self-deploying-workflow.md). Self-deploying mode uses the Enrollment Status Page (ESP) to hold the device in a provisioning state. It also prevents the user from proceeding to the desktop after enrollment but before applications and configurations are done applying. If the ESP is disabled, the **Reseal** button might appear before applications and configurations are done applying. Disabling the ESP might advertently allow proceeding to the user flow before technician flow provisioning is complete. The success status screen validates that enrollment was successful, not that the technician flow is necessarily complete. For this reason, Microsoft recommends not to disable the ESP. Instead enable the ESP as suggested in the **Configure and assign Windows Autopilot Enrollment Status Page (ESP)** step.

## Next step: User flow

[Step 9: User flow](azure-ad-join-user-flow.md)

## Related content

For more information on the technician flow of a Windows Autopilot for pre-provisioned deployment, see the following articles:

- [Technician flow](../../pre-provision.md#technician-flow).
