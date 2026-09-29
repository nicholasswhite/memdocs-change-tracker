---
title: "Windows Autopilot device preparation user-driven Microsoft Entra join: Allow users to join devices to Microsoft Entra ID"
description: How to - Windows Autopilot device preparation user-driven Microsoft Entra join - Step 2 of 7 - Allow users to join devices to Microsoft Entra ID.
ms.date: "2026-08-07T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
---

# Windows Autopilot device preparation user-driven Microsoft Entra join: Allow users to join devices to Microsoft Entra ID

Windows Autopilot device preparation user-driven Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](entra-join-automatic-enrollment.md)

- **Step 2: Allow users to join devices to Microsoft Entra ID**

- Step 3: [Create an assigned device group](entra-join-device-group.md)
- Step 4: [Create a user group](entra-join-user-group.md)
- Step 5: [Assign applications and PowerShell scripts to device group](entra-join-assign-apps-scripts.md)
- Step 6: [Create Windows Autopilot device preparation policy](entra-join-autopilot-policy.md)
- Step 7, option 1: [Add Windows corporate identifier to device](entra-join-corporate-identifier.md)
- Step 7, option 2: [Associate devices](entra-join-device-association.md)

For an overview of the Windows Autopilot device preparation user-driven Microsoft Entra join workflow, see [Windows Autopilot device preparation user-driven Microsoft Entra join overview](entra-join-workflow.md#workflow).

> [!NOTE]
>
> If users are already allowed to join devices to Microsoft Entra ID, skip this step and move on to [Step 3: Create an assigned device group](entra-join-device-group.md).

## Allow users to join devices to Microsoft Entra ID

In order for Windows Autopilot device preparation to work, users need to be allowed to join devices to Microsoft Entra ID. Allowing users to join devices to Microsoft Entra ID can be configured in the [Azure portal](https://portal.azure.com):

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

## Next step: Create an assigned device group

[Step 3: Create an assigned device group](entra-join-device-group.md)

## Related content

For more information on allowing users to join devices to Microsoft Entra ID, see the following articles:

- [Configure device settings](https://learn.microsoft.com/en-us/azure/active-directory/devices/device-management-azure-portal#configure-device-settings).
