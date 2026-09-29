---
title: "Add the Windows Company Portal app by using Microsoft Intune"
description: Learn how your workforce can manually add the Windows Company Portal app to their PC from the Microsoft Store.
ms.date: "2026-01-06T00:00:00Z"
ms.topic: how-to
ms.collection:
- M365-identity-device-management
- Windows
---

# Add the Windows Company Portal app by using Microsoft Intune

To manage devices and install apps, your users can install the Company Portal app themselves from the Microsoft Store. If your business needs require that you assign the Company Portal app to them, however, you can assign the Company Portal app for Windows directly from Intune.

> [!IMPORTANT]
>
> To deploy the Company Portal app for Windows Autopilot provisioned devices, see [Add Company Portal app for Windows Autopilot devices](add-company-portal-autopilot.md).

> [!NOTE]
>
> The Company Portal supports Configuration Manager applications. This feature allows end users to see both Configuration Manager and Intune deployed applications in the Company Portal for co-managed customers. The Company Portal displays Configuration Manager deployed apps for all co-managed customers. This support helps administrators consolidate their different end user portal experiences. For more information, see [Use the Company Portal app on co-managed devices](../../configmgr/comanage/company-portal.md).

## Download the Company Portal app using Windows Package Manager

1. Use the [Windows Package Manager](https://learn.microsoft.com/en-us/windows/package-manager/winget/download) command-line tool to download the Company Portal app for Windows with dependencies by entering the following command:

   ```powershell
   winget download "Company Portal" --source msstore
   ```

   By default, files are downloaded to the user's Downloads folder. Use the `--download-directory` option to specify a custom download path.
2. In the Microsoft Intune admin center, upload the Company Portal app as a new app.

   1. Go to **Apps** &gt; **Platforms** and select **Windows**.
   2. Select **Add**.
   3. For **App type**, choose **Other** &gt; **Line-of-business app**.
   4. Choose **Select** to continue.
   5. On the **App information** page, choose **Select app package file**.
   6. In the new pane, select the **File** upload button, and then upload the app package file. The file you want to select has the app package (.appxbundle) extension.
3. Detected dependencies appear. Under **Select dependency app files**, select all dependencies you downloaded in step 1.

   1. **Shift + click** to select all dependencies.
   2. Under the **Added** column, verify that **Yes** appears for the architectures you need.

   > [!NOTE]
   >
   > If you don't add the dependencies, installation could fail for the selected device types.
4. Select **OK**.
5. Under **App information**, enter any information about the app.
6. Select **Add**.
7. Assign the Company Portal app as a required app to selected users or device groups.

For more information about how Intune handles dependencies for Universal apps, see [Deploying an appxbundle with dependencies via Microsoft Intune MDM](https://learn.microsoft.com/en-us/archive/blogs/configmgrdogs/deploying-an-appxbundle-with-dependencies-via-microsoft-intune-mdm).

## Next steps

- [Assign apps to groups](assign-groups.md)
