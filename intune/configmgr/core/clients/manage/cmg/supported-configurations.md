---
title: "Supported configurations for cloud management gateway"
description: A list of the features and configurations that the Configuration Manager cloud management gateway supports.
ms.date: "2022-07-12T00:00:00Z"
ms.subservice: core-infra
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# Supported configurations for cloud management gateway

*Applies to: Configuration Manager (current branch)*

Use this article as a reference for the features and configurations that are supported by the Configuration Manager cloud management gateway (CMG).

## Specifications

- All Windows versions listed in [Supported operating systems for clients and devices](../../../plan-design/configs/supported-operating-systems-for-clients-and-devices.md) are supported for CMG.
- CMG only supports the management point and software update point roles.
- CMG doesn't support clients that only communicate with IPv6 addresses.
- Software update points using a network load balancer don't work with CMG.
- Starting in version 2203, the option to deploy a CMG as a **cloud service (classic)** is removed. All CMG deployments should use a [virtual machine scale set](plan-cloud-management-gateway.md#virtual-machine-scale-sets). For more information, see [Removed and deprecated features](../../../plan-design/changes/deprecated/removed-and-deprecated-cmfeatures.md).
- CMG names need to be between 3-24 alphanumeric characters. The name must begin with a letter, end with a letter or digit, and not contain consecutive hyphens.

## Support for Configuration Manager features

The following table lists CMG support for Configuration Manager features:

| Feature | Support |
| --- | --- |
| Software updates | ![Supported.](media/green-check.png) |
| Endpoint protection | ![Supported.](media/green-check.png) <sup>[Note 1](#bkmk_note1)</sup> |
| Hardware and software inventory | ![Supported.](media/green-check.png) |
| Client status and notifications | ![Supported.](media/green-check.png) |
| Run scripts | ![Supported.](media/green-check.png) |
| CMPivot | ![Supported.](media/green-check.png) |
| Compliance settings | ![Supported.](media/green-check.png) |
| Automatic client upgrade | ![Supported.](media/green-check.png) |
| Client install (with [Microsoft Entra integration](../../deploy/deploy-clients-cmg-azure.md)) | ![Supported.](media/green-check.png) |
| Client install (with [token authentication](../../deploy/deploy-clients-cmg-token.md)) | ![Supported.](media/green-check.png) |
| Software distribution (device-targeted) | ![Supported.](media/green-check.png) |
| Software distribution (user-targeted, required) (with Microsoft Entra integration) | ![Supported.](media/green-check.png) |
| Software distribution (user-targeted, available) ([all requirements](../../../../apps/plan-design/prerequisites-deploy-user-available-apps.md)) | ![Supported.](media/green-check.png) |
| BitLocker Management | ![Supported.](media/green-check.png) |
| Pull distribution point source | ![Supported.](media/green-check.png) |
| Windows [in-place upgrade task sequence](../../../../osd/deploy-use/create-a-task-sequence-to-upgrade-an-operating-system.md) <sup>[Note 2](#bkmk_note2)</sup> | ![Supported.](media/green-check.png) |
| Task sequence without a boot image, deployed with the option to **Download all content locally before starting task sequence** <sup>[Note 2](#bkmk_note2)</sup> | ![Supported.](media/green-check.png) |
| Task sequence without a boot image, deployed with [either download option](../../../../osd/deploy-use/deploy-task-sequence-over-internet.md#deploy-windows-in-place-upgrade-via-cmg) <sup>[Note 2](#bkmk_note2)</sup> | ![Supported.](media/green-check.png) |
| Task sequence with a boot image, started from Software Center <sup>[Note 2](#bkmk_note2)</sup> | ![Supported.](media/green-check.png) |
| Task sequence with a boot image, started from bootable media <sup>[Note 2](#bkmk_note2)</sup> | ![Supported.](media/green-check.png) |
| Any other task sequence scenario <sup>[Note 2](#bkmk_note2)</sup> | ![Not supported.](media/red-x.png) |
| Content for PXE or multicast-enabled deployments | ![Not supported.](media/red-x.png) |
| Client push | ![Not supported.](media/red-x.png) |
| Automatic site assignment | ![Not supported.](media/red-x.png) |
| Software approval requests | ![Not supported.](media/red-x.png) |
| Configuration Manager console | ![Not supported.](media/red-x.png) |
| Remote tools | ![Not supported.](media/red-x.png) <sup>[Note 3](#bkmk_note3)</sup> |
| Reporting website | ![Not supported.](media/red-x.png) |
| Wake on LAN | ![Not supported.](media/red-x.png) |
| macOS clients | ![Not supported.](media/red-x.png) |
| Peer cache | ![Not supported.](media/red-x.png) |
| On-premises MDM | ![Not supported.](media/red-x.png) |
| Alternate content providers | ![Not supported.](media/red-x.png) <sup>[Note 4](#bkmk_note4)</sup> |
| Content for App-V streaming applications | ![Not supported.](media/red-x.png) |
| Content for Microsoft 365 Apps updates | ![Not supported.](media/red-x.png) |
| [Prestage content](../../../plan-design/hierarchy/manage-network-bandwidth.md#BKMK_PrestagingContent) | ![Not supported.](media/red-x.png) |

| Key |
| --- |
| ![Supported.](media/green-check.png) = This feature is supported with CMG by all supported versions of Configuration Manager |
| ![Supported.](media/green-check.png) (*YYMM*) = This feature is supported with CMG starting with version *YYMM* of Configuration Manager |
| ![Not supported.](media/red-x.png) = This feature isn't supported with CMG |

### Support notes

#### Note 1: Support for endpoint protection

Clients that communicate via a CMG can immediately apply endpoint protection policies without an active connection to Active Directory.

#### Note 2: Support for task sequences

For more information about support for deploying a task sequence to a client via the CMG, see [Deploy a task sequence over the internet](../../../../osd/deploy-use/deploy-task-sequence-over-internet.md).

#### Note 3: Support for remote tools

As announced at Microsoft Ignite 2021, a public preview of the new remote assistance solution is now available in the Microsoft Intune admin center. This cloud-based tool can help you more securely support users of Windows devices.

For more information, see the following resources:

- [Remote Help: a new remote assistance tool from Microsoft (blog post)](https://techcommunity.microsoft.com/t5/microsoft-endpoint-manager-blog/remote-help-a-new-remote-assistance-tool-from-microsoft/ba-p/2822622)
- [Enable remote help scenarios with Microsoft Intune (demo video)](https://techcommunity.microsoft.com/t5/video-hub/enable-remote-help-scenarios-with-microsoft-endpoint-manager/ba-p/2911349)
- [Use Remote Help with Intune and Configuration Manager](../../../../../remote-help/index.md)

#### Note 4: Support for alternate content providers

Alternate content providers aren't supported to get content from a content-enabled CMG. You can still use them on a client that communicates with a CMG and gets content from other supported content locations.

> [!TIP]
>
> Starting in version 2203, you can also configure the task sequence to allow token authentication with alternate content providers. For more information, see [Task sequence variables: SMSTSAllowTokenAuthURLForACP](../../../../osd/understand/task-sequence-variables.md#smstsallowtokenauthurlforacp).

## Next steps

Next, plan how the design the CMG for the best performance at the appropriate scale:

[CMG performance and scale](perf-scale.md)
