---
title: "Pre-provision Microsoft Entra join: User flow"
description: How to - Windows Autopilot for pre-provisioned deployment Microsoft Entra join - Step 8 of 9 - User flow.
ms.date: "2024-07-23T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Pre-provision Microsoft Entra join: User flow

Windows Autopilot for pre-provisioned deployment Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](azure-ad-join-automatic-enrollment.md)
- Step 2: [Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)
- Step 3: [Register devices as Windows Autopilot devices](azure-ad-join-register-device.md)
- Step 4: [Create a device group](azure-ad-join-device-group.md)
- Step 5: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](azure-ad-join-esp.md)
- Step 6: [Create and assign Windows Autopilot profile](azure-ad-join-autopilot-profile.md)
- Step 7: [Assign Windows Autopilot device to a user (optional)](azure-ad-join-assign-device-to-user.md)
- Step 8: [Technician flow](azure-ad-join-technician-flow.md)

- **Step 9: User flow**

For an overview of the Windows Autopilot for pre-provisioned deployment Microsoft Entra join workflow, see [Windows Autopilot for pre-provisioned deployment Microsoft Entra join overview](azure-ad-join-workflow.md#workflow).

## User flow

Once the technician flow step of the pre-provisioning process completes successfully and the device is resealed, the device can be delivered to the end-user. The end-user then completes the normal Windows Autopilot user-driven process. This final step is know as the user flow and involves the following steps:

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

4. Once the Windows Autopilot process begins, the Microsoft Entra sign-in page appears. At the Microsoft Entra sign-in page, if a user was assigned to the device, their username might be pre-populated in this screen. Enter the Microsoft Entra credentials for the user and then select **Next** (Windows 10) or **Sign in** (Windows 11) to sign in. If necessary, proceed through the multi-factor authentication (MFA) screens.
5. After authenticating with Microsoft Entra ID, the Enrollment Status Page (ESP) appears. The Enrollment Status Page (ESP) appears. The Enrollment Status Page (ESP) displays progress during the provisioning process across three phases:

   - **Device preparation** (Device ESP)
   - **Device setup** (Device ESP)
   - **Account setup** (User ESP)

   The first two phases of **Device preparation** and **Device setup** are part of the Device ESP while the final phase of **Account setup** is part of the User ESP.

   For the user flow of Windows Autopilot for pre-provisioned deployment, the **Device setup** phase of the Device ESP and the **Account setup** phase of the User ESP runs. The **Device preparation** phase of the Device ESP doesn't run during the user flow since it already ran during the [Technician flow](azure-ad-join-technician-flow.md).

   The **Device setup** phase of the Device ESP runs again during the user flow in case any new or additional policies or applications assigned to the device became available between the technician flow phase and the user flow phase.
6. Once **Account setup** and the user ESP process completes, the provisioning process completes, the ESP finishes, and the desktop appears. At this point, the end-user can start using the device.

## User-flow tips

- Depending on how the Windows Autopilot profile was configured at the **Create and assign Windows Autopilot profile** step, additional screens might appear during the Windows Autopilot deployment appear such as:  
     
  - **Language**/**Country**/**Region** or **Keyboard** screens before the Microsoft Entra sign-in page.
  - **Privacy** screen when the user ESP/**Account setup** begins but before the user is automatically signed in.

- To view and hide detailed progress information in the ESP during the provisioning process:  
     
  - **Windows 10**: To show details, next to the appropriate phase select **Show details**. To hide the details, next to the appropriate phase select **Hide details**.
  - **Windows 11**: To show details, next to the appropriate phase select **∨**. To hide the details, next to the appropriate phase select **∧**.

- For tokens to refresh properly between the Technician flow and the User flow, wait at least 90 minutes after running the Technician flow before running the User flow. This scenario mainly affects lab and testing scenarios, such as this tutorial, when the User flow is run within 90 minutes after the Technician flow completes.
- The User flow should be run within six months after the Technician flow finishes. Waiting more than six months can cause the certificates used by the Intune Management Engine (IME) to no longer be valid leading to errors such as:

  `Error code: [Win32App][DetectionActionHandler] Detection for policy with id: <policy_id> resulted in action status: Failed and detection state: NotComputed.`

- Compliance in Microsoft Entra ID is reset during the User flow. Devices might show as compliant in Microsoft Entra ID after the Technician flow completes, but then show as noncompliant once the User flow starts. Allow enough time after the User flow completes for compliance to reevaluate and update.

## Related content

For more information on the user flow of a Windows Autopilot for pre-provisioned deployment, see the following articles:

- [User flow](../../pre-provision.md#user-flow).
