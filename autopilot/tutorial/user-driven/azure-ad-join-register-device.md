---
title: "User-driven Microsoft Entra join: Register devices as Windows Autopilot devices"
description: How to - Windows Autopilot user-driven Microsoft Entra join - Step 3 of 8 - Register devices as Windows Autopilot devices.
ms.date: "2025-03-25T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# User-driven Microsoft Entra join: Register devices as Windows Autopilot devices

Windows Autopilot user-driven Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](azure-ad-join-automatic-enrollment.md)
- Step 2: [Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)

- **Step 3: Register devices as Windows Autopilot devices**

- Step 4: [Create a device group](azure-ad-join-device-group.md)
- Step 5: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](azure-ad-join-esp.md)
- Step 6: [Create and assign Windows Autopilot profile](azure-ad-join-autopilot-profile.md)
- Step 7: [Assign Windows Autopilot device to a user (optional)](azure-ad-join-assign-device-to-user.md)
- Step 8: [Deploy the device](azure-ad-join-deploy-device.md)

For an overview of the Windows Autopilot user-driven Microsoft Entra join workflow, see [Windows Autopilot user-driven Microsoft Entra join overview](azure-ad-join-workflow.md#workflow).

> [!NOTE]
>
> If devices are already registered as Windows Autopilot devices, skip this step and move on to [Step 4: Create a device group](azure-ad-join-device-group.md).

## Register devices as Windows Autopilot devices

Before a device can use Windows Autopilot, the device must be registered as a Windows Autopilot device. Registering a device as a Windows Autopilot device can be thought of as importing the device into Windows Autopilot so that Windows Autopilot service can be used on the device. Registering a device as a Windows Autopilot device doesn't mean that the device has used the Windows Autopilot service. It just makes the Windows Autopilot service available to the device.

Also note that a device registered in Windows Autopilot doesn't mean the device is enrolled in Intune. A device might be registered as a Windows Autopilot device but might not exist in Intune. It's not until a Windows Autopilot registered device goes through the Windows Autopilot process for the first time that it becomes enrolled in Intune. After the Windows Autopilot device undergoes the Windows Autopilot process and enrolls in Intune, the Windows Autopilot device appears as a device in both Microsoft Entra ID and Intune.

There are several methods to register a device as a Windows Autopilot device in Intune:

- Manually registering devices into Intune as a Windows Autopilot device via the hardware hash. The hardware hash of a device can be collected via one of the following methods:

  - [Configuration Manager](../../../intune/configmgr/comanage/how-to-prepare-Win10.md#windows-autopilot).
  - [PowerShell script](../../add-devices.md#powershell).
  - [Diagnostics page hash export](../../add-devices.md#diagnostics-page-hash-export).
  - [Desktop hash export](../../add-devices.md#desktop-hash-export).

  These methods of obtaining the hardware hash of a device are well documented. The corresponding documentation can be viewed by selecting the appropriate link from the above list.
- Automatically registering device via:

  - An [OEM](../../oem-registration.md), including [Microsoft Surface](https://learn.microsoft.com/en-us/surface/surface-autopilot-registration-support) devices.
  - A [partner](../../partner-registration.md).

  Registering a device via an OEM or partner is also well documented. The corresponding documentation can be viewed by selecting the appropriate link from the above list.

For most organizations, using an OEM or partner to register devices as Windows Autopilot devices is the preferred, most common, and most secure method. However for smaller organizations, for testing/lab scenarios, and for emergency scenarios, manually registering devices as Windows Autopilot devices via the hardware hash is also used.

> [!IMPORTANT]
>
> The following type of devices shouldn't be registered as a Windows Autopilot device:
>
> - [Microsoft Entra registered](https://learn.microsoft.com/en-us/entra/identity/devices/concept-device-registration) devices, also known as "workplace joined" devices.
> - [Intune MDM-only enrollment](https://learn.microsoft.com/en-us/intune/device-enrollment/enroll-devices?tabs=byod-enrollment#windows-enrollment-methods) devices.
>
> These options are intended for users to join personally owned devices to their organization's network. Windows Autopilot registered devices are registered as corporate owned devices.
>
> If a device is already one of these two types of devices, to register is as a Windows Autopilot device, first remove it from Microsoft Intune and Microsoft Entra ID. For more information, see [Why is the join type for a device showing as "Microsoft Entra registered" instead of "Microsoft Entra joined"?](../../troubleshooting-faq.yml#why-is-the-join-type-for-a-device-showing-as--microsoft-entra-registered--instead-of--microsoft-entra-joined--) and [Deregister a device](../../registration-overview.md#deregister-a-device).

> [!NOTE]
>
> Assuming that a device isn't currently enrolled Intune, remember that registering a device in Windows Autopilot doesn't make it an Intune enrolled device. That device doesn't enroll into Intune until Windows Autopilot runs on the device for the first time.

## Importing the hardware hash CSV file for devices into Intune

Several of the methods in the previous section on obtaining the hardware hash when manually registering devices as Windows Autopilot devices produces a CSV file that contains the hardware hash of the device. This CSV file with the hardware hash needs to be imported into Intune to register the device as a Windows Autopilot device.

After the CSV file is created, it can be imported into Intune via the following steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left hand pane.
3. In the **Devices | Overview** screen, under **By platform**, select **Windows**.
4. In the **Windows | Windows devices** screen, under **Device onboarding**, select **Enrollment**.
5. In the **Windows | Windows enrollment** screen, under **Windows Autopilot**, select **Devices**.
6. In the **Windows Autopilot devices** screen that opens, select **Import**.

   1. In the **Add Autopilot devices** window that opens:

      1. Under **Specify the path to the list you want to import.**, select the blue file folder.
      2. Browse to the CSV file obtained using one of the above methods to obtain the hardware hash of a device.
      3. After selecting the CSV file, verify that the correct CSV file is selected under **Specify the path to the list you want to import.**, and then select **Import**. Selecting **Import** closes the **Add Autopilot devices** window. Importing can take several minutes.
   2. After the import is complete, select **Sync**.

      A message displays saying that the sync is in progress. The sync process might take a few minutes to complete, depending on how many devices are being synchronized.

      > [!NOTE]
      >
      > If another sync is attempted within 10 minutes after initiating a sync, an error will be displayed. Syncs can only occur once every 10 minutes. To attempt a sync again, wait at least 10 minutes before trying again.
   3. Select **Refresh** to refresh the view. The newly imported devices should display within a few minutes. If the devices aren't yet displayed, wait a few minutes, and then select **Refresh** again.

## Next step: Create a device group

[Step 4: Create a device group](azure-ad-join-device-group.md)

## Related content

For more information on registering devices as Windows Autopilot devices, see the following articles:

- [Manually register devices with Windows Autopilot](../../add-devices.md).
- [Windows Autopilot customer consent](../../registration-auth.md).
