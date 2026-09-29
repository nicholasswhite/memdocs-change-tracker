---
title: "User-driven Microsoft Entra join: Assign Windows Autopilot device to a user (optional)"
description: How to - Windows Autopilot user-driven Microsoft Entra join - Step 7 of 8 - Assign Windows Autopilot device to a user.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# User-driven Microsoft Entra join: Assign Windows Autopilot device to a user (optional)

Windows Autopilot user-driven Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](azure-ad-join-automatic-enrollment.md)
- Step 2: [Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)
- Step 3: [Register devices as Windows Autopilot devices](azure-ad-join-register-device.md)
- Step 4: [Create a device group](azure-ad-join-device-group.md)
- Step 5: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](azure-ad-join-esp.md)
- Step 6: [Create and assign Windows Autopilot profile](azure-ad-join-autopilot-profile.md)

- **Step 7: Assign Windows Autopilot device to a user (optional)**

- Step 8: [Deploy the device](azure-ad-join-deploy-device.md)

For an overview of the Windows Autopilot user-driven Microsoft Entra join workflow, see [Windows Autopilot user-driven Microsoft Entra join overview](azure-ad-join-workflow.md#workflow).

## Assign Windows Autopilot device to a user (optional)

A device that is registered as a Windows Autopilot device can also be assigned to a user. If a Windows Autopilot device is assigned to a user, then any user policies and application installs assigned to that user is applied to the device during the Windows Autopilot process.

> [!TIP]
>
> For testing purposes, especially for hybrid Microsoft Entra scenarios, it might be better to first test a Windows Autopilot deployment before assigning the device to a user. Not assigning a user limits the scope of applications, policies, and configurations processed during the Windows Autopilot process.

> [!TIP]
>
> For Configuration Manager admins, assigning a user to a device is similar to user device affinity in Configuration Manager.

To assign a Windows Autopilot device to a user, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left hand pane.
3. In the **Devices | Overview** screen, under **By platform**, select **Windows**.
4. In the **Windows | Windows devices** screen, under **Device onboarding**, select **Enrollment**.
5. In the **Windows | Windows enrollment** screen, under **Windows Autopilot**, select **Devices**.
6. In the **Windows Autopilot devices** screen that opens, locate the device to assign a user to.
7. Once the desired device is located, select the box to the left of the device, making sure that there's check mark in the box, and then select **Assign user** in the toolbar at the top of page.
8. In the **Select user** window that opens, find and select a user for the device, and then select **Select** to close the window. If necessary, use the **Search** box to find the desired user.

   > [!NOTE]
   >
   > The selected user must be an Azure user licensed to use Intune.
9. In the Windows Autopilot device's property window that automatically opens on the right hand side, under **User friendly name**, verify the default value. If the value is empty or a different friendly name is desired, enter the desired friendly name for the user under **User friendly name**, and then select **Save** to close the property window.
10. The user assignment can be verified by selecting the Windows Autopilot device in the **Windows Autopilot devices** screen. Once the Windows Autopilot device is selected, it highlights and the Windows Autopilot device's property window automatically opens on the right hand side. The assigned user is listed under **User** and **User friendly name**.

## Assigning Windows Autopilot device to a user via hardware hash CSV file

A user can be manually assigned to a Windows Autopilot device in the Windows Autopilot device's properties. However, a user can also be assigned to the Windows Autopilot device when the device was initially imported into Windows Autopilot as a Windows Autopilot device. Assigning a user when the device is imported as a Windows Autopilot device can be done by editing the hardware hash CSV file and adding the **Assigned User** column after the **Hardware Hash** column. The user's User Principal Name (UPN) should then be added as a value under the **Assigned User** column.

> [!IMPORTANT]
>
> Use a plain-text editor such as **Notepad** to edit the CSV file. Don't use Microsoft Excel. Editing the CSV file in Excel doesn't generate a proper usable file for importing into Intune.

For more information on editing the CSV file to add an assigned user to the Windows Autopilot device, see [Manually register devices with Windows Autopilot: Ensure that the CSV file meets requirements](../../add-devices.md#ensure-that-the-csv-file-meets-requirements).

## Next step: Deploy the device

[Step 8: Deploy the device](azure-ad-join-deploy-device.md)

## Related content

For more information on assigning a user to a Windows Autopilot device, see the following article:

- [Assign a user to a specific Windows Autopilot device](../../enrollment-autopilot.md#assign-a-user-to-a-specific-windows-autopilot-device).
