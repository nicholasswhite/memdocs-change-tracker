---
title: "Windows Autopilot device preparation in automatic mode for Windows 365: Set up Windows automatic Intune enrollment"
description: How to - Windows Autopilot device preparation in automatic mode for Windows 365 - Step 1 of 6 - Set up Windows automatic Intune enrollment.
ms.date: "2025-06-11T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
author: lenewsad
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4b132a0c-342a-42eb-91ff-8159e1ed413d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/72cb4d1c-66f7-4281-99d5-e04a64d084fc
manager: laurawi
moniker_range_name: ''
ms.author: lanewsad
ms.reviewer: madakeva
ms.service: windows-client
ms.subservice: autopilot
ms.suite: ems
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/d9ebaec0-4879-449e-9781-0afdce99fe0a
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/f2b71146-ce8e-46a8-9965-8aa8b3aa8235
---

# Windows Autopilot device preparation in automatic mode for Windows 365: Set up Windows automatic Intune enrollment

Windows Autopilot device preparation in automatic mode for Windows 365 steps:

- **Step 1: Set up Windows automatic Intune enrollment**

- Step 2: [Create an assigned device group](automatic-device-group.md)
- Step 3: [Assign applications and PowerShell scripts to device group](automatic-assign-apps-scripts.md)
- Step 4: [Create Windows Autopilot device preparation policy](automatic-autopilot-policy.md)
- Step 5: [Create a Cloud PC provisioning policy](automatic-cloud-pc-provisioning-policy.md)
- Step 6: [Monitor the deployment](automatic-monitor.md)

For an overview of the Windows Autopilot device preparation in automatic mode for Windows 365 workflow, see [Windows Autopilot device preparation in automatic mode for Windows 365 overview](automatic-workflow.md#workflow).

> [!NOTE]
>
> If automatic Intune enrollment is already set up, skip this step and move on to [Step 2: Create an assigned device group](automatic-device-group.md).

## Set up Windows automatic Intune enrollment

In order for Windows Autopilot device preparation to work, devices need to be able to enroll in Intune automatically. Enrolling devices in Intune automatically can be configured in the [Azure portal](https://portal.azure.com):

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

## Next step: Create an assigned device group

[Step 2: Create an assigned device group](automatic-device-group.md)

## Related content

For more information on Windows automatic MDM/Intune enrollment, see the following articles:

- [Enable Windows automatic enrollment](https://learn.microsoft.com/en-us/intune/intune-service/enrollment/windows-enroll#enable-windows-automatic-enrollment).
- [Set up Windows automatic enrollment](../../../windows-autopilot-hybrid.md#set-up-windows-automatic-mdm-enrollment).
