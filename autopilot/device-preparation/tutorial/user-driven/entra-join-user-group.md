---
title: "Windows Autopilot device preparation user-driven Microsoft Entra join: Create a user group"
description: How to - Windows Autopilot device preparation user-driven Microsoft Entra join - Step 4 of 7 - Create a user group.
ms.date: "2026-08-07T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
---

# Windows Autopilot device preparation user-driven Microsoft Entra join: Create a user group

Windows Autopilot device preparation user-driven Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](entra-join-automatic-enrollment.md)
- Step 2: [Allow users to join devices to Microsoft Entra ID](entra-join-allow-users-to-join.md)
- Step 3: [Create an assigned device group](entra-join-device-group.md)

- **Step 4: Create a user group**

- Step 5: [Assign applications and PowerShell scripts to device group](entra-join-assign-apps-scripts.md)
- Step 6: [Create Windows Autopilot device preparation policy](entra-join-autopilot-policy.md)
- Step 7, option 1: [Add Windows corporate identifier to device](entra-join-corporate-identifier.md)
- Step 7, option 2: [Associate devices](entra-join-device-association.md)

For an overview of the Windows Autopilot device preparation user-driven Microsoft Entra join workflow, see [Windows Autopilot device preparation user-driven Microsoft Entra join overview](entra-join-workflow.md#workflow).

> [!NOTE]
>
> The user group created in this step is specific to Windows Autopilot device preparation. Microsoft recommends creating a user group specifically for use with Windows Autopilot device preparation instead of reusing existing user groups used in other Windows Autopilot scenarios.

## Create a user group

User groups are a collection of users organized into a Microsoft Entra group. User groups can be either dynamic or assigned:

- **Dynamic groups** - Users are automatically added to the group based on rules.
- **Assigned groups** - Users are manually added to the group and are static.

Windows Autopilot device preparation uses a user group as part of the Windows Autopilot device preparation policy. The users that are members of the user group specified in the Windows Autopilot device preparation policy are the users that receive the Windows Autopilot device preparation deployment. The user group specified in the Windows Autopilot device preparation policy needs to be a security group but can be either an assigned or dynamic group.

To create a user security group for use with Windows Autopilot device preparation, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Groups** in the left hand pane.
3. In the **Groups | All groups** screen, make sure **All groups** is selected, and then select **New group**.
4. In the **New Group** screen that opens:

   1. For **Group type**, select **Security**.
   2. For **Group name**, enter a name for the user group, such as **Windows Autopilot device preparation user group**.
   3. For **Group description**, enter a description for the user group.
   4. For **Microsoft Entra roles can be assigned to the group**, select **No**.
   5. For **Membership type**:

      - Select **Assigned** to create an assigned user group.
      - Select **Dynamic User** to create a dynamic user group.
   6. For **Owners**, select the **No owners selected** link.
   7. In the **Add owners** screen that opens:

      1. Scroll through the list of objects and select owners for the user group. Alternatively, use the **Search** bar to search for and select owners of the group.
      2. Once all of the desired owners are selected, select **Select**.
   8. For assigned user groups:

      1. For **Members**, select the **No members selected** link.
      2. In the **Add members** screen that opens:

         1. Scroll through the list of objects and select members that the Windows Autopilot device preparation profiles should be deployed to. Alternatively, use the **Search** bar to search for and select members for the group. Make sure to only select users or groups that only contain users.
         2. Once all of the desired users or user groups are selected that the Windows Autopilot device preparation profiles should be deployed to, select **Select**.
   9. For dynamic user groups:

      1. For **Dynamic user members**, select the **Add dynamic query** link.
      2. In the **Dynamic membership rules** screen that opens, create a rule that encompasses the users that should be members of the user group. For more information on creating rules, see [Dynamic membership rules for groups in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/users/groups-dynamic-membership).

      > [!NOTE]
      >
      > The linked article is in regards to creating dynamic membership rules in Microsoft Entra ID. However, dynamic user groups in Intune are also dynamic user groups in Microsoft Entra ID, so the rule syntax is the same.
   10. Select **Create** to finish creating user group.

## Next step: Assign applications and PowerShell scripts to device group

[Step 5: Assign applications and PowerShell scripts to device group](entra-join-assign-apps-scripts.md)

## Related content

For more information on creating groups in Intune, see the following articles:

- [Create device groups](../../../enrollment-autopilot.md).
- [Add groups to organize users and devices](../../../../intune/fundamentals/tenant-administration/add-groups.md).
- [Manage Microsoft Entra groups and group membership](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/how-to-manage-groups).
- [Dynamic membership rules for groups in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/users/groups-dynamic-membership).
