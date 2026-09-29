---
title: "Pre-provision Microsoft Entra join: Allow users to join devices to Microsoft Entra ID"
description: How to - Windows Autopilot for pre-provisioned deployment Microsoft Entra join - Step 2 of 9 - Allow users to join devices to Microsoft Entra ID.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Pre-provision Microsoft Entra join: Allow users to join devices to Microsoft Entra ID

Windows Autopilot for pre-provisioned deployment Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](azure-ad-join-automatic-enrollment.md)

- **Step 2: Allow users to join devices to Microsoft Entra ID**

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
> If users are already allowed to join devices to Microsoft Entra ID, skip this step and move on to [Step 3: Register devices as Windows Autopilot devices](azure-ad-join-register-device.md).

## Allow users to join devices to Microsoft Entra ID

In order for Windows Autopilot to work, users need to be allowed to join devices to Microsoft Entra ID. Allowing users to join devices to Microsoft Entra ID can be configured in the [Azure portal](https://portal.azure.com):

1. Sign in to the [Azure portal](https://portal.azure.com/).
2. Select **Microsoft Entra ID**.
3. In the **Overview** screen, under **Manage** in the left hand pane, select **Devices**.
4. In the **Devices | Overview** screen, under **Manage** in the left hand pane, select **Device Settings**.
5. In the **Devices | Device settings** screen that opens, under **Users may join devices to Microsoft Entra**, select either **All** or **Selected**:

   - If **All** is selected, all users can join their devices to Microsoft Entra ID.
   - If **Some** is selected, only users specified under **Selected** can join their devices to Microsoft Entra ID. To add users:

     1. Select the link under **Selected**.
     2. In the **Members allowed to join devices** page that opens:

        1. Select **Add**.
        2. In the **Add members** window that opens:

           1. Select the desired users and/or groups to add.
           2. Once all of the desired users and groups are selected, select **Select** to close the **Add members** window.
        3. Select **OK**.

        > [!NOTE]
        >
        > Any selected groups must be a Microsoft Entra group that contains user objects.
6. In the **Devices | Overview** screen, if any changes were made, select **Save**.

> [!NOTE]
>
> This step of allowing users to join devices to Microsoft Entra ID is only needed for the Windows Autopilot user-driven Microsoft Entra join and Windows Autopilot for pre-provisioned deployment Microsoft Entra join scenarios. This setting doesn't apply to Microsoft Entra hybrid joined devices and Microsoft Entra joined devices using Windows Autopilot self-deployment mode as these methods work in a userless context.

## Next step: Register devices as Windows Autopilot devices

[Step 3: Register devices as Windows Autopilot devices](azure-ad-join-register-device.md)

## Related content

For more information on allowing users to join devices to Microsoft Entra ID, see the following articles:

- [Configure device settings](https://learn.microsoft.com/en-us/azure/active-directory/devices/device-management-azure-portal#configure-device-settings).
