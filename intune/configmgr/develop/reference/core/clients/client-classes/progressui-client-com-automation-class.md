---
description: Learn how the ProgressUI is a COM automation class in Configuration Manager that represents a user interface that custom actions use to report progress to the Configuration Manager operating system deployment task sequencing environment.
title: ProgressUI Client COM Automation Class
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43093068-2dda-408b-b3fe-dfd705c84f78
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/e453d60d-ba7e-43bc-8028-ec38e6b62512
---

# ProgressUI Client COM Automation Class

`ProgressUI` is a COM automation class in Configuration Manager that represents a user interface that custom actions use to report progress to the Configuration Manager operating system deployment task sequencing environment. The class implements the `IProgressUI` interface, which has a method `ShowActionProgress` that is used to display custom action progress information in a dialog box while the custom action is running. You shouldn't call any other method implemented in `ProgressUI`.

## In This Section

| Term | Definition |
| --- | --- |
| [IProgressUI Interface](iprogressui-interface.md) | Manages custom action progress information. |

## Remarks

`ProgressUI` is implemented in TSProgressUI.exe.

The class GUID is F79474A1-7B80-4a18-BC7B-D3938BD93808.

The programmatic identifier (ProgID) is Microsoft.SMS.TsProgressUI.

To use `ProgressUI` in Visual Studio, add a reference to "SMS TSE Progress UI."

## See Also

[Operating System Deployment Client COM Automation Classes](operating-system-deployment-client-com-automation-classes.md) [About Reporting Configuration Manager Custom Action Progress](../../../../osd/about-reporting-configuration-manager-custom-action-progress.md)
