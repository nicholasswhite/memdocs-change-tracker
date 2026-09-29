---
title: "Pre-provision Microsoft Entra join: Set up Windows automatic Intune enrollment"
description: How to - Windows Autopilot for pre-provisioned deployment Microsoft Entra join - Step 1 of 9 - Set up Windows automatic Intune enrollment.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Pre-provision Microsoft Entra join: Set up Windows automatic Intune enrollment

Windows Autopilot for pre-provisioned deployment Microsoft Entra join steps:

- **Step 1: Set up Windows automatic Intune enrollment**

- Step 2: [Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)
- Step 3: [Register devices as Windows Autopilot devices](azure-ad-join-register-device.md)
- Step 4: [Create a device group](azure-ad-join-device-group.md)
- Step 5: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](azure-ad-join-esp.md)
- Step 6: [Create and assign Windows Autopilot profile](azure-ad-join-autopilot-profile.md)
- Step 7: [Assign Windows Autopilot device to a user (optional)](azure-ad-join-assign-device-to-user.md)
- Step 8: [Technician flow](azure-ad-join-technician-flow.md)
- Step 9: [User flow](azure-ad-join-user-flow.md)

For an overview of the Windows Autopilot for pre-provisioned deployment Microsoft Entra join workflow, see [Windows Autopilot for pre-provisioned deployment Microsoft Entra join overview](azure-ad-join-workflow.md#workflow).

> [!NOTE]
>
> If automatic Intune enrollment is already set up, skip this step and move on to [Step 2: Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md).

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

[Step 2: Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)

## Related content

For more information on Windows automatic MDM/Intune enrollment, see the following articles:

- [Enable Windows automatic enrollment](https://learn.microsoft.com/en-us/intune/intune-service/enrollment/windows-enroll#enable-windows-automatic-enrollment).
- [Set up Windows automatic enrollment](../../windows-autopilot-hybrid.md#set-up-windows-automatic-mdm-enrollment).
