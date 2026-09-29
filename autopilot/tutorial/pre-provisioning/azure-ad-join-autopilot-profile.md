---
title: "Pre-provision Microsoft Entra join: Create and assign a pre-provisioned Microsoft Entra join Windows Autopilot profile"
description: How to - Windows Autopilot for pre-provisioned deployment Microsoft Entra join - Step 6 of 9 - Create and assign a pre-provisioned Microsoft Entra join Windows Autopilot profile.
ms.date: "2025-06-13T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 10</a>
---

# Pre-provision Microsoft Entra join: Create and assign a pre-provisioned Microsoft Entra join Windows Autopilot profile

Windows Autopilot for pre-provisioned deployment Microsoft Entra join steps:

- Step 1: [Set up Windows automatic Intune enrollment](azure-ad-join-automatic-enrollment.md)
- Step 2: [Allow users to join devices to Microsoft Entra ID](azure-ad-join-allow-users-to-join.md)
- Step 3: [Register devices as Windows Autopilot devices](azure-ad-join-register-device.md)
- Step 4: [Create a device group](azure-ad-join-device-group.md)
- Step 5: [Configure and assign Windows Autopilot Enrollment Status Page (ESP)](azure-ad-join-esp.md)

- **Step 6: Create and assign Windows Autopilot profile**

- Step 7: [Assign Windows Autopilot device to a user (optional)](azure-ad-join-assign-device-to-user.md)
- Step 8: [Technician flow](azure-ad-join-technician-flow.md)
- Step 9: [User flow](azure-ad-join-user-flow.md)

For an overview of the Windows Autopilot for pre-provisioned deployment Microsoft Entra join workflow, see [Windows Autopilot for pre-provisioned deployment Microsoft Entra join overview](azure-ad-join-workflow.md#workflow).

## Create and assign a pre-provisioned Microsoft Entra join Windows Autopilot profile

The Windows Autopilot profile specifies how the device is configured during Windows Setup and what is shown during the out-of-box experience (OOBE).

When an admin creates a Windows Autopilot profile for the pre-provisioned scenario, devices with this Windows Autopilot profile are associated with the user enrolling the device. User credentials are required to enroll the device.

The difference between a Windows Autopilot pre-provisioned Microsoft Entra join and a Windows Autopilot Microsoft Entra hybrid join is that the pre-provisioned Microsoft Entra join scenario only joins Microsoft Entra ID during Windows Autopilot. The Microsoft Entra hybrid join scenario joins both an on-premises domain and Microsoft Entra ID during Windows Autopilot.

> [!TIP]
>
> For Configuration Manager admins, the Windows Autopilot profile is similar to some of the configuration that takes place during a task sequence via an `unattend.xml` file. The `unattend.xml` file is configured during the **Apply Windows Settings** and **Apply Network Settings** steps. Windows Autopilot doesn't use `unattend.xml` files.

To create a pre-provisioned Microsoft Entra join Windows Autopilot profile, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left hand pane.
3. In the **Devices | Overview** screen, under **By platform**, select **Windows**.
4. In the **Windows | Windows devices** screen, under **Device onboarding**, select **Enrollment**.
5. In the **Windows | Windows enrollment** screen, under **Windows Autopilot**, select **Deployment Profiles**.
6. In the **Windows Autopilot deployment profiles** screen, select the **Create Profile** drop down menu and then select **Windows PC**.
7. The **Create profile** screen opens. In the **Basics** page:

   1. Next to **Name**, enter a name for the Windows Autopilot profile.
   2. Next to **Description**, enter a description.
   3. Select **Next**.

      > [!NOTE]
      >
      > Microsoft recommends setting the option **Convert all targeted devices to Autopilot** to **Yes**. This tutorial concentrates on new devices where the device is manually imported as a Windows Autopilot device using the hardware hash. However, this option can be helpful when assigning Windows Autopilot profiles to device groups that contain existing devices. For example, this option is helpful when using the [Windows Autopilot for existing devices](../existing-devices/existing-devices-workflow.md) scenario. With Windows Autopilot for existing devices, existing devices might need to be registered as a Windows Autopilot device after the Windows Autopilot deployment completes. For more information, see [Register device for Windows Autopilot](../existing-devices/register-device.md).

8. In the **Out-of-box experience (OOBE)** page:

   - For **Deployment mode**, select **User-driven**.
   - For **Join to Microsoft Entra ID as**, select **Microsoft Entra joined**.
   - For **Microsoft Software License Terms**, select **Hide** to skip the EULA page.
   - For **Privacy settings**, select **Hide** to skip the privacy settings.
   - For **Hide change account options**, select **Hide**.
   - For **User account type**, select the desired account type for the user (**Administrator** or **Standard** user). If **Administrator** is chosen, the user is added to the local Admin group.
   - For **Allow pre-provisioned deployment**, select **Yes**.
   - For **Language (Region)**, select **Operating system default** to use the default language for the operating system being configured. If another language is desired, select the desired language from the drop-down list.
   - For **Automatically configure keyboard**, select **Yes** to skip the keyboard selection page.
   - For **Apply device name template**, select **No**. Alternatively, **Yes** can be chosen to apply a device name template. Be aware of the following if the name template is selected to **Yes**:

     - Names must be 15 characters or less, and can have letters, numbers, and hyphens.
     - Names can't be all numbers.
     - Use the [%SERIAL% macro](https://learn.microsoft.com/en-us/windows/client-management/mdm/accounts-csp) to add a hardware-specific serial number.
     - Use the [%RAND:x% macro](https://learn.microsoft.com/en-us/windows/client-management/mdm/accounts-csp) to add a random string of numbers, where x equals the number of digits to add.

   > [!NOTE]
   >
   > The above settings are selected to minimize needed user interaction during device setup. However, some of the settings that are hidden can instead be shown as desired. For example, some regions might require that **Privacy settings** always be shown.

   > [!NOTE]
   >
   > If the language/region and keyboard screens are set to hidden, they might still be displayed if there's no network connectivity at the start of the Windows Autopilot deployment. When there's no network connectivity at the start of the deployment, the Windows Autopilot profile, where the settings to hide these screens is defined, hasn't downloaded yet. Once network connectivity is established, the Windows Autopilot profile is downloaded and any additional screen settings should work as expected.

9. Once the options in the **Out-of-box experience (OOBE)** page are configured as desired, select **Next**.
10. In the **Assignments** page:

    1. Under **Included groups**, select **Add groups**.

    > [!NOTE]
    >
    > Make sure to add the correct device groups under **Included groups** and not under **Excluded groups**. Accidentally adding the desired device groups under **Excluded groups** prevents devices in those device groups from receiving the Windows Autopilot profile.

    1. In the **Select groups to include** window that opens, select the groups that the Windows Autopilot profile should be assigned to. These device groups are normally the device groups created in the previous **Create device group** step. Once done, select **Select**.
    2. Under **Included groups** &gt; **Groups**, ensure the correct groups are selected, and then select **Next**.
11. In the **Review + Create** page, verify that all settings are set correctly, and then select **Create** to create the Windows Autopilot profile.

## Verify device has a Windows Autopilot profile assigned to it

Before deploying a device, ensure that a Windows Autopilot profile is assigned to a device group that the device is a member of. Windows Autopilot profile assignment to a device can take some time after the Windows Autopilot profile is assigned to the device group or after the device is added to the device group. To verify that the profile is assigned to a device, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Devices** in the left hand pane.
3. In the **Devices | Overview** screen, under **By platform**, select **Windows**.
4. In the **Windows | Windows devices** screen, under **Device onboarding**, select **Enrollment**.
5. In the **Windows | Windows enrollment** screen, under **Windows Autopilot**, select **Devices**.
6. In the **Windows Autopilot devices** screen that opens:

   1. Find the desired device that Windows Autopilot deployment profile assignment status needs to be checked.
   2. Once the device is located, its current status is listed under the **Profile status** column. The status has one of the following values:

      - **Not assigned**: A Windows Autopilot deployment profile isn't assigned to the device.
      - **Assigning**: A Windows Autopilot deployment profile is being assigned to the device.
      - **Assigned**: A Windows Autopilot deployment profile is assigned to the device.
      - **Fix pending**: When a hardware change occurs on a device, this status displays while Intune tries to register the new hardware. When the link for the **Fix pending** status is selected, the following message appears:

        **We've detected a hardware change on this device. We're trying to automatically register the new hardware. You don't need to do anything now; the status will be updated at the next check in with the result.**

        If Intune is able to successfully register the new hardware, Intune updates the profile status when the device next checks into Intune. For more information on the **Fix pending** status, see the following articles:

        - [Why is the Windows Autopilot profile not applied after a hardware change occurred on a device?](../../troubleshooting-faq.yml#why-is-the-windows-autopilot-profile-not-applied-after-a-hardware-change-occurred-on-a-device-).
        - [Return of key functionality for Windows Autopilot sign-in and deployment experience](https://techcommunity.microsoft.com/t5/intune-customer-success/return-of-key-functionality-for-windows-autopilot-sign-in-and/ba-p/3583130).
        - [Windows Autopilot motherboard replacement scenario guidance](../../autopilot-motherboard-replacement.md)
      - **Attention required**: If Intune is unable to register the new hardware after a hardware change occurs on a device, the device can't receive the Windows Autopilot profile until the device is reset and the device re-registers. For more information on this status and how to deregister/re-register a device, see the following articles:

        - [Why is the Windows Autopilot profile not applied after a hardware change occurred on a device?](../../troubleshooting-faq.yml#why-is-the-windows-autopilot-profile-not-applied-after-a-hardware-change-occurred-on-a-device-).
        - [Return of key functionality for Windows Autopilot sign-in and deployment experience](https://techcommunity.microsoft.com/t5/intune-customer-success/return-of-key-functionality-for-windows-autopilot-sign-in-and/ba-p/3583130).
        - [Windows Autopilot motherboard replacement scenario guidance](../../autopilot-motherboard-replacement.md)
        - [Deregister a device](../../registration-overview.md#deregister-a-device)

      Before starting the Windows Autopilot deployment process on a device, make sure that in the **Windows Autopilot devices** page:

      - The device's **Profile status** status is **Assigned**.
      - In the properties of the device, **Date assigned** has a value.
      - In the properties of the device, **Assigned profile** displays the expected Windows Autopilot profile.

> [!NOTE]
>
> Intune periodically checks for new devices in the assigned device groups, and then begins the process of assigning profiles to those devices. Due to several different factors involved in the process of Windows Autopilot profile assignment, an estimated time for the assignment can vary from scenario to scenario. These factors can include Microsoft Entra groups, membership rules, hash of a device, Intune and Windows Autopilot services, and internet connection. The assignment time varies depending on all the factors and variables involved in a specific scenario.

## Next step: Assign Windows Autopilot device to a user (optional) or Technician flow

[Step 7: Assign Windows Autopilot device to a user (optional)](azure-ad-join-assign-device-to-user.md)

If a user isn't being assigned to the device, then skip to **[Step 8: Technician flow](azure-ad-join-technician-flow.md)**.

[Step 8: Technician flow](azure-ad-join-technician-flow.md)

## Related content

For more information on configuring Windows Autopilot profiles, see the following articles:

- [Configure Windows Autopilot profiles](../../profiles.md).
