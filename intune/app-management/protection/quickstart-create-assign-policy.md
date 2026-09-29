---
title: "Step 9 - Create and assign an app protection policy in Microsoft Intune"
description: Learn how to create and assign an app protection policy in Microsoft Intune to protect your organization's data. Get step-by-step guidance.
ms.topic: how-to
ms.date: "2026-01-20T00:00:00Z"
ms.reviewer: dagerrit
ms.collection:
- M365-identity-device-management
- FocusArea_Apps_Protect
---

# Step 9 - Create and assign an app protection policy in Microsoft Intune

In this article, you learn how to create and assign an app protection policy in Microsoft Intune to protect apps on user devices. App protection policies help ensure your apps meet your organization's data protection requirements, keeping corporate data secure.

This article is [part of an Evaluate and Try series](../../fundamentals/try-overview.md) that helps you evaluate Microsoft Intune's capabilities.

## Prerequisites

![](../../media/icons/16/licensing.svg) **Licensing requirements**

> - A Microsoft Intune subscription. [Sign up for a free trial account](../../fundamentals/free-trial-sign-up.md).

![](../../media/icons/16/rbac.svg) **Roles requirements**

> Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) with the following role:
>
> - Built-in **[Application Manager](../../fundamentals/role-based-access-control/ref-built-in-roles.md#application-manager)** Microsoft Intune role

![](../../media/icons/16/configuration.svg) **Device configuration requirements**

> To complete this step, you must:
>
> - [Create a user](../../fundamentals/tenant-administration/quickstart-create-user.md).
> - [Create a group](../../fundamentals/tenant-administration/quickstart-create-group.md).
> - [Enroll a device](../../device-enrollment/windows/quickstart-automatic-mdm.md)
> - [Add and assign an app](../deployment/quickstart-add-assign.md).

## Create an app protection policy

Use the following steps to create an app protection policy:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) and select **Apps** &gt; **Windows** &gt; **Create**.
2. Enter the following details:

   - **Name**: *Windows content protection*
   - **Description**: *Users associated with this policy can't cut, copy, or paste any content between the assigned app and other nonmanaged apps on the device.*
   - **Enrollment state**: *With enrollment*
3. Under **Protected apps**, select **Add**. The **Add apps** pane is displayed.
4. Choose the apps that must adhere to this policy and select **OK**.
5. Select **Next** to display the **Required settings**.
6. Select **Allow Overrides** to set the Windows Information Protection mode. Selecting this option blocks enterprise data from leaving the protected app.
7. Select **Next** to display the **Advanced settings**.
8. Select **Next** to display the **Assignments**.
9. Select **Select groups to include**, select the users group, and select **Select**.

   You can only apply app protection policies to groups that contain users, not groups that contain devices.
10. Select **Next** to display the **Review + create** step.
11. Select **Create** to create your policy.

You see the app protection policy in Intune.

## Next steps

In this article, you created and assigned an app protection policy. Users of the app that have this policy assigned can't cut, copy, or paste any content between the assigned app and other unmanaged apps on the device. This type of protection helps protect your organization's data. For more information about app protection policies in Intune, see [What are app protection policies?](overview.md)

To continue evaluating Microsoft Intune, go to the next step:

[Step 10 - Create and assign a custom role](../../fundamentals/role-based-access-control/quickstart-custom-role.md)
