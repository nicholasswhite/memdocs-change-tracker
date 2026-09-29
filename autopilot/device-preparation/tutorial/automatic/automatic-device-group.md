---
title: "Windows Autopilot device preparation in automatic mode for Windows 365: Create an assigned device group"
description: How to - Windows Autopilot device preparation in automatic mode for Windows 365 - Step 2 of 6 - Create an assigned device group.
ms.date: "2025-06-11T00:00:00Z"
ms.topic: tutorial
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
---

# Windows Autopilot device preparation in automatic mode for Windows 365: Create an assigned device group

Windows Autopilot device preparation in automatic mode for Windows 365 steps:

- Step 1: [Set up Windows automatic Intune enrollment](automatic-automatic-enrollment.md)

- **Step 2: Create an assigned device group**

- Step 3: [Assign applications and PowerShell scripts to device group](automatic-assign-apps-scripts.md)
- Step 4: [Create Windows Autopilot device preparation policy](automatic-autopilot-policy.md)
- Step 5: [Create a Cloud PC provisioning policy](automatic-cloud-pc-provisioning-policy.md)
- Step 6: [Monitor the deployment](automatic-monitor.md)

For an overview of the Windows Autopilot device preparation in automatic mode for Windows 365 workflow, see [Windows Autopilot device preparation in automatic mode for Windows 365 overview](automatic-workflow.md#workflow).

> [!NOTE]
>
> The device group created in this step is specific to Windows Autopilot device preparation. Microsoft recommends creating a device group specifically for use with Windows Autopilot device preparation instead of reusing existing device groups used in other Windows Autopilot scenarios.

## Create an assigned device group

Device groups are a collection of devices or Cloud PCs organized into a Microsoft Entra group. Normally device groups can be either assigned or dynamic:

- **Assigned groups** - Devices or Cloud PCs are manually added to the group and are static. Windows Autopilot device preparation only uses assigned groups.
- **Dynamic groups** - Devices or Cloud PCs are automatically added to the group based on rules. Windows Autopilot device preparation doesn't use dynamic groups.

Windows Autopilot device preparation uses an **assigned device group** as part of the Windows Autopilot device preparation policy. The device group specified in the Windows Autopilot device preparation policy needs to be an **assigned device group**. The Windows Autopilot device preparation process then adds devices or Cloud PCs automatically to this assigned device group during the Windows Autopilot device preparation deployment.

> [!IMPORTANT]
>
> The device group specified in the Windows Autopilot device preparation policy needs to be an **assigned security device group**.

> [!TIP]
>
> Although the same assigned device group can be used for multiple Windows Autopilot device preparation policies, Microsoft recommends creating a separate assigned device group for each Windows Autopilot device preparation policy. For example, a different assigned device group for a user-driven scenario vs. an automatic scenario. Creating a separate assigned device group allows for easier management of the Windows Autopilot device preparation policies and the devices or Cloud PCs that are assigned to them.

To create an assigned security device group for use with Windows Autopilot device preparation, follow these steps:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. In the **Home** screen, select **Groups** in the left hand pane.
3. In the **Groups | All groups** screen, make sure **All groups** is selected, and then select **New group**.
4. In the **New Group** screen that opens:

   1. For **Group type**, select **Security**.
   2. For **Group name**, enter a name for the device group, such as **Windows Autopilot device preparation device group**.
   3. For **Group description**, enter a description for the device group.
   4. For **Microsoft Entra roles can be assigned to the group**, select **No**.
   5. For **Membership type**, select **Assigned**.
   6. For **Owners**, select the **No owners selected** link.
   7. In the **Add owners** screen that opens:

      1. Scroll through the list of objects and select the service principal **Intune Provisioning Client** with AppId of **f1346770-5b25-470b-88bd-d5744ab7952c**. Alternatively, use the **Search** bar to search for and select **Intune Provisioning Client**.

         > [!NOTE]
         >
         > - In some tenants, the service principal might have the name of **Intune Autopilot ConfidentialClient** instead of **Intune Provisioning Client**. As long as the AppID of the service principal is **f1346770-5b25-470b-88bd-d5744ab7952c**, it's the correct service principal.
         > - If the **Intune Provisioning Client** or **Intune Autopilot ConfidentialClient** service principal with AppId of **f1346770-5b25-470b-88bd-d5744ab7952c** isn't available either in the list of objects or when searching, see [Adding the Intune Provisioning Client service principal](#adding-the-intune-provisioning-client-service-principal).
      2. Once **Intune Provisioning Client** is selected as the owner, select **Select**.
   8. Select **Create** to finish creating the assigned device group.

   > [!IMPORTANT]
   >
   > Devices are automatically added to this device group during the Windows Autopilot device preparation deployment. Manually adding devices as members of the device group created in this step isn't necessary, but doing so has no impact on the Windows Autopilot device preparation process.

### Adding the Intune Provisioning Client service principal

If the **Intune Provisioning Client** service principal with AppId **f1346770-5b25-470b-88bd-d5744ab7952c** isn't available when selecting the owner of the device group, then follow these steps to add the service principal:

1. On a device where Microsoft Intune or Microsoft Entra ID is normally administered, open an elevated **Windows PowerShell** command prompt.
2. In the **Windows PowerShell** command prompt window:

   1. Install the **Microsoft.Graph.Authentication** module by entering the following command:

      ```powershell
      Install-Module Microsoft.Graph.Authentication
      ```

      If prompted to do so:

      - Agree to install **NuGet** by entering **Y** or **Yes**, or selecting the **Yes** button.
      - Agree to install from the **PSGallery** untrusted repository by entering **Y** or **Yes**, or selecting the **Yes** button.

      For more information, see [Microsoft.Graph.Authentication](https://learn.microsoft.com/en-us/powershell/module/microsoft.graph.authentication/) and [Set-PSRepository -InstallationPolicy](https://learn.microsoft.com/en-us/powershell/module/powershellget/set-psrepository#-installationpolicy).
   2. Install the **Microsoft.Graph.Applications** module by entering the following command:

      ```powershell
      Install-Module Microsoft.Graph.Applications
      ```

      If prompted to do so, agree to install from the **PSGallery** untrusted repository by entering **Y** or **Yes**, or selecting the **Yes** button.

      For more information, see [Microsoft.Graph.Applications](https://learn.microsoft.com/en-us/powershell/module/microsoft.graph.applications/) and [Set-PSRepository -InstallationPolicy](https://learn.microsoft.com/en-us/powershell/module/powershellget/set-psrepository#-installationpolicy).
   3. Once the **Microsoft.Graph.Authentication** and **Microsoft.Graph.Applications** modules are installed, connect to Microsoft Entra ID by entering the following command:

      ```powershell
      Connect-MgGraph -Scopes "Application.ReadWrite.All"
      ```

      For more information, see [Connect-MgGraph](https://learn.microsoft.com/en-us/powershell/module/microsoft.graph.authentication/connect-mggraph).
   4. If not already authenticated to Microsoft Entra ID, the **Sign in to your account** window appears. Enter the credentials of a Microsoft Entra ID administrator that has permissions to add service principals.
   5. If the **Permissions requested** window appears, select the **Consent on behalf of your organization** checkbox, and then select the **Accept** button.
   6. Once authenticated to Microsoft Entra ID and proper permissions are granted, add the **Intune Provisioning Client** service principal by entering the following command:

      ```powershell
      New-MgServicePrincipal -AppID f1346770-5b25-470b-88bd-d5744ab7952c
      ```

      For more information, see [New-MgServicePrincipal -BodyParameter](https://learn.microsoft.com/en-us/powershell/module/microsoft.graph.applications/new-mgserviceprincipal#-bodyparameter).

      > [!NOTE]
      >
      > - The following error message is displayed if the **Intune Provisioning Client service principal** already exists in the tenant:
      >
      >   ```powershell
      >   New-MgServicePrincipal : The service principal cannot be created, updated, or restored because the service principal name
      >   f1346770-5b25-470b-88bd-d5744ab7952c is already in use.
      >   Status: 409 (Conflict)
      >   ErrorCode: Request_MultipleObjectsWithSameKeyValue
      >   ```
      > - The following error message is displayed if one of the following conditions is true:
      >
      >   - The account used to sign in with the `Connect-MgGraph` command doesn't have permissions to add a service principal to the tenant.
      >   - The `-Scopes "Application.ReadWrite.All"` argument isn't added to the `Connect-MgGraph` command.
      >   - The **Permissions requested** window isn't accepted.
      >   - The **Consent on behalf of your organization** checkbox isn't selected in the **Permissions requested** window.
      >
      >   ```powershell
      >   New-MgServicePrincipal : Insufficient privileges to complete the operation.
      >   Status: 403 (Forbidden)
      >   ErrorCode: Authorization_RequestDenied
      >   ```

## Next step: Assign applications and PowerShell scripts to device group

[Step 3: Assign applications and PowerShell scripts to device group](automatic-assign-apps-scripts.md)

## Related content

For more information on creating groups in Intune, see the following articles:

- [Create device groups](../../../enrollment-autopilot.md).
- [Add groups to organize users and devices](../../../../intune/fundamentals/tenant-administration/add-groups.md).
- [Manage Microsoft Entra groups and group membership](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/how-to-manage-groups).
- [Dynamic membership rules for groups in Microsoft Entra ID](https://learn.microsoft.com/en-us/entra/identity/users/groups-dynamic-membership).
