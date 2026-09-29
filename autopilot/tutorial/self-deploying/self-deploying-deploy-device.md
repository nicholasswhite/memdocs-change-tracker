---
title: "Self-deploying mode: Deploy the device"
description: How to - Windows Autopilot self-deploying mode - Step 5 of 5 - Step 6 of 6 - Deploy the device.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Self-deploying mode: Deploy the device

Windows Autopilot self-deploying mode steps:

- Step 1: [Set up Windows automatic Intune enrollment](self-deploying-automatic-enrollment.md)
- Step 2: [Register devices as Windows Autopilot devices](self-deploying-register-device.md)
- Step 3: [Create a device group](self-deploying-device-group.md)
- Step 4: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](self-deploying-esp.md)
- Step 5: [Create and assign Windows Autopilot profile](self-deploying-autopilot-profile.md)

- **Step 6: Deploy the device**

For an overview of the Windows Autopilot self-deploying mode workflow, see [Windows Autopilot self-deploying overview](self-deploying-workflow.md#workflow).

## Deploy the device

Once all of the configurations for the Windows Autopilot self-deploying deployment are on the Intune and Microsoft Entra ID side, the next step is to start the Windows Autopilot deployment process on the device. If desired, deploy any additional applications and policies that should run during the Windows Autopilot deployment to a device group that the device is a member of.

To start the Windows Autopilot deployment process on the device, acquire a device that is part of the device group created in the previous [Create a device group](self-deploying-device-group.md) step. Once the device is acquired, follow these steps:

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

4. The Enrollment Status Page (ESP) appears. The Enrollment Status Page (ESP) displays progress during the provisioning process across three phases:

   - **Device preparation** (Device ESP)
   - **Device setup** (Device ESP)
   - **Account setup** (User ESP)

   The first two phases of **Device preparation** and **Device setup** are part of the Device ESP while the final phase of **Account setup** is part of the User ESP. For Windows Autopilot self-deploying mode, only the Device ESP and its related two related phases (**Device preparation** and **Device setup**) run. User ESP and **Account setup** don't run until after the Windows Autopilot self-deploying deployment is complete and a user signs in.
5. Once **Device setup** and the device ESP process completes, the Windows Autopilot self-deploying deployment is complete, and the Windows sign-on screen appears.
6. At this point, the end-user can sign in to the device using their Microsoft Entra credentials. When the user signs in, the user ESP and **Account setup** phase runs. Once user ESP and **Account setup** completes, the provisioning process completes, the desktop appears, and the end-user can start using the device.

## Deployment tips

- Before the Windows Autopilot deployment is started, Microsoft recommends having:

  - At least one type of policy and at least one application assigned to the devices.
  - At least one type of policy and at least one application assigned to the users.

  These assignments ensure proper testing of the Windows Autopilot deployment during the Device ESP phase. It might also prevent possible issues when there are either no policies or no applications assigned to the device.
- For Windows Autopilot self-deploying mode:

  - Any user assigned to the device is ignored during the Windows Autopilot self-deploying deployment.
  - User ESP doesn't run until after the Windows Autopilot self-deploying deployment completes and a user signs in.

  However, for testing purposes, assigning at least one policy and at least one application to users is still recommended.
- Depending on how the Windows Autopilot profile was configured at the [Create and assign Windows Autopilot profile](self-deploying-autopilot-profile.md) step, the **Keyboard** screen might appear at the start of the deployment.

- To view and hide detailed progress information in the ESP during the provisioning process:  
     
  - **Windows 10**: To show details, next to the appropriate phase select **Show details**. To hide the details, next to the appropriate phase select **Hide details**.
  - **Windows 11**: To show details, next to the appropriate phase select **∨**. To hide the details, next to the appropriate phase select **∧**.
