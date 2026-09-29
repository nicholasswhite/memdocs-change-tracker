---
title: "Remove association from a device"
description: "Remove a Windows Autopilot device association by deleting the device from the Device association list in Intune or by clearing the Device Link UEFI variables on the device."
ms.date: "2026-09-11T00:00:00Z"
ms.topic: how-to
appliesto:
  - ✅ <a href="https://learn.microsoft.com/windows/release-health/supported-versions-windows-client" target="_blank">Windows 11</a>
---

# Remove association from a device

When a device permanently leaves your organization—for example, when it's decommissioned or transferred to another organization—remove its Windows Autopilot device association so the device is no longer tied to your tenant. For an associated device, removal clears the trusted tenant affiliation from the device's UEFI storage. How you remove the association depends on whether the device has completed association in the out-of-box experience (OOBE).

> [!NOTE]
>
> Removing a device from the **Device association** list in Intune doesn't clear the tenant affinity that's stored on an already associated device. To fully remove the association from an associated device, clear the association information on the device itself, and then delete the device from the **Device association** list.

## Remove device in a pre-associated state

If the device hasn't completed association in OOBE yet (its state is **Pre-associated**), delete it directly from the device list:

1. Sign in to the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431).
2. Go to **Devices** &gt; **Enrollment** &gt; **Device association** &gt; **Devices**.
3. Select the device, and then select **Delete**.

The device is removed from the list immediately.

## Remove device in an associated state

If the device already completed association (its state is **Associated**), the tenant affinity is stored in the device's UEFI firmware. Clear the association information on the device first, and then delete the device from Intune.

Before clearing the association, make sure the device is no longer enrolled with its mobile device management (MDM) provider as part of your decommissioning process. If the device remains enrolled, the MDM provider attempts to re-associate it on its next check-in.

The association is stored in the **Device Link** UEFI namespace. Clear all of the following variables to remove the association:

| UEFI namespace | Variable |
| --- | --- |
| `{B3DE75DA-819C-4FD5-9F01-C3D49E8CBBD7}` | `DeviceLinkId` |
| `{B3DE75DA-819C-4FD5-9F01-C3D49E8CBBD7}` | `DeviceLinkJwtCompressed` |
| `{B3DE75DA-819C-4FD5-9F01-C3D49E8CBBD7}` | `DeviceLinkJwtLastWrite` |
| `{B3DE75DA-819C-4FD5-9F01-C3D49E8CBBD7}` | `DeviceLinkCreationTimeUtc` |

> [!IMPORTANT]
>
> Clearing the Device Link UEFI variables only removes the association. It doesn't reset the TPM, unenroll the device, or delete the device's Microsoft Entra ID or Intune records.

### Delete the device from Intune

After you clear the association information on the device, remove the device record from Intune:

1. In the [Microsoft Intune admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Devices** &gt; **Enrollment** &gt; **Device association** &gt; **Devices**.
2. Select the device. The **Association state** changes to **Pending removal**.
3. Select **Delete** to remove the device from the list.

   > [!NOTE]
   >
   > The **Pending removal** state indicates that the removal request was submitted. The device disappears from the list once the process completes.

## Related content

- [Overview of Windows Autopilot device association](overview.md)
- [Device association lifecycle management](lifecycle-management.md)
