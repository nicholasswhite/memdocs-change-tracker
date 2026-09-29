---
title: "Edit device properties in Microsoft Intune"
description: "Learn how to edit the modifiable properties of a managed device on the Properties tab in the Microsoft Intune admin center, including the device name, ownership, primary user, notes, and scope tags."
ms.date: "2026-07-05T00:00:00Z"
---

# Edit device properties in Microsoft Intune

Each managed device has a set of properties that you can change from the **Properties** tab in the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431). These editable properties are separate from the read-only information on the **Device details** tab. For the read-only details, see [View device details](device-details.md).

The **Properties** tab lets you edit:

- **Intune device name** — the device name shown in the admin center. See [Rename a device](rename-device.md).
- **Ownership** — whether the device is corporate or personal.
- **Primary user** — the user primarily associated with the device.
- **Device notes** — free-form text to record admin context.
- **Scope tags** — tags that control which admins can see and manage the device.

## Open the Properties tab

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431) and select [**Devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/overview) &gt; [**All devices**](https://go.microsoft.com/fwlink/?linkid=2109431#view/Microsoft_Intune_DeviceSettings/DevicesMenu/%7E/allDevices).
2. From the devices list, select a device.
3. Select the **Properties** tab, and then select **Edit**.
4. Change the properties you want to update, and then save your changes.

The rest of this article describes each editable property.

## Change ownership

Ownership identifies a device as **corporate** or **personal**. Ownership affects the management capabilities available for the device and the information Intune collects from it. On the **Properties** tab, select the ownership value that matches how the device is used in your organization, and then save your changes.

## Change the primary user

The primary user is the user primarily associated with the device (also known as *device affinity*). You change or remove a device's primary user from the **Properties** tab. For the steps, requirements, and important considerations—plus background on how the primary user is assigned—see [Change the primary user](find-primary-user.md#change-the-primary-user).

## Add device notes

Use **Notes** to record admin context about the device, such as its purpose, location, or a support reference. Notes are visible to admins in the admin center. Add or update the text on the **Properties** tab, and then save your changes.

## Edit scope tags

Scope tags control which admins can see and manage the device, based on their role assignments. In the device's **Scope tags** section, add or remove tags to align device visibility with your distributed IT model. For more information, see [Use role-based access control and scope tags for distributed IT](../../fundamentals/role-based-access-control/scope-tags.md).

> [!TIP]
>
> You can also [assign a device category](../create-device-categories.md#change-the-category-of-a-device) to automatically group the device for easier management.

## Next steps

- [Rename a device](rename-device.md)
- [View device details](device-details.md)
