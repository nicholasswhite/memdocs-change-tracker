---
title: IAppContentExt Interface
description: In Configuration Manager, the IAppContentExt interface defines functions to retrieve the application content information. The interface inherits from IUnknown.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/540ac133-a371-4dbb-8f94-28d6cc77a70b
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
spProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/60bfc045-f127-4841-9d00-ea35495a5800
---

# IAppContentExt Interface

The `IAppContentExt` interface, in Configuration Manager, defines functions to retrieve the application content information.

The interface inherits from `IUnknown`.

## In This Section

The following table lists the methods in the `IAppContentExt` interface.

| Term | Definition |
| --- | --- |
| [IAppContentExt::GetExcludedFileList](iappcontentext--getexcludedfilelist.md) | Gets the excluded file list for an application's content. This is used to support selective file download. |

## Remarks

.

## UUID

The UUID for `IAppContentExt` is 1537EE1C-30AC-4c92-A2BE-6B3A3903E249.

## See Also

[Application Management Client Interfaces](application-management-client-interfaces.md) [Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
