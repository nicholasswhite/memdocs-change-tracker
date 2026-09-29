---
title: "Self-deploying mode: Set up Windows automatic Intune enrollment"
description: How to - Windows Autopilot self-deploying mode - Step 1 of 5 - Set up Windows automatic Intune enrollment.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Self-deploying mode: Set up Windows automatic Intune enrollment

Windows self-deploying mode steps:

- **Step 1: Set up Windows automatic Intune enrollment**

- Step 2: [Register devices as Windows Autopilot devices](self-deploying-register-device.md)
- Step 3: [Create a device group](self-deploying-device-group.md)
- Step 4: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](self-deploying-esp.md)
- Step 5: [Create and assign Windows Autopilot profile](self-deploying-autopilot-profile.md)
- Step 6: [Deploy the device](self-deploying-deploy-device.md)

For an overview of the Windows Autopilot self-deploying mode workflow, see [Windows Autopilot self-deploying overview](self-deploying-workflow.md#workflow).

> [!NOTE]
>
> If automatic Intune enrollment is already set up, skip this step and move on to [Step 2: Register devices as Windows Autopilot devices](self-deploying-register-device.md).

## Set up Windows automatic Intune enrollment

In order for Windows Autopilot to work, devices need to be able to enroll in Intune automatically. Enrolling devices in Intune automatically can be configured in the [Azure portal](https://portal.azure.com):

1. Sign in to the [Azure portal](https://portal.azure.com/).
2. Select **Microsoft Entra ID**.
3. In the **Overview** screen, under **Manage** in the left hand pane, select **Mobility (MDM and WIP)**.
4. In the **Mobility (MDM and WIP)** screen, under **Name** select **Microsoft Intune**.
5. In the **Microsoft Intune** page that opens, under **MDM user scope**, select either **All** or **Some**:

   - If **All** is selected, all users can automatically enroll their devices in Intune.
   - If **Some** is selected, only users in the groups specified in the link under **Groups** can automatically enroll their devices in Intune. To add groups:

     1. Select the link under **Groups**.
     2. In the **Select groups** window that opens, select the desired groups to add. Make sure that the groups selected are Microsoft Entra user groups that contain the desired users.
     3. Once all of the desired groups are selected, select **Select** to close the **Select groups** window.
6. In the **Microsoft Intune** screen, if any changes were made, select **Save**.

## Next step: Allow users to join devices to Microsoft Entra ID

[Step 2: Register devices as Windows Autopilot devices](self-deploying-register-device.md)

## Related content

For more information on Windows automatic MDM/Intune enrollment, see the following articles:

- [Enable Windows automatic enrollment](https://learn.microsoft.com/en-us/intune/intune-service/enrollment/windows-enroll#enable-windows-automatic-enrollment).
- [Set up Windows automatic enrollment](../../windows-autopilot-hybrid.md#set-up-windows-automatic-mdm-enrollment).
