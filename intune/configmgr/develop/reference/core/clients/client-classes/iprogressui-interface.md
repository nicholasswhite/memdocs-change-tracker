---
title: IProgressUI interface
description: IProgressUI represents the user interface that allows custom actions to report progress to the OS deployment task sequencing environment.
ms.date: "2019-04-03T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43093068-2dda-408b-b3fe-dfd705c84f78
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# IProgressUI interface

The `IProgressUI` automation interface in Configuration Manager represents the user interface that allows custom actions to report progress to the OS deployment task sequencing environment.

## Methods for this interface

| Term | Definition |
| --- | --- |
| [IProgressUI::CloseProgressDialog](iprogressui--closeprogressdialog-method.md) | Closes open instances of `IProgressUI` |
| [IProgressUI::ShowActionProgress](iprogressui--showactionprogress-method.md) | Displays custom action progress information in a dialog box while the custom action is running. |
| [IProgressUI::ShowErrorDialog](iprogressui--showerrordialog-method.md) | Displays customizable error information in a dialog box. |
| [IProgressUI::ShowMessage](iprogressui--showmessage-method.md) | Displays customizable dialog box. |
| [IProgressUI::ShowMessageEx](iprogressui--showmessageex-method.md) | Displays customizable dialog box and captures an integer result variable. |
| [IProgressUI::ShowRebootDialog](iprogressui--showrebootdialog-method.md) | Displays customizable reboot warning dialog box. |
| [IProgressUI::ShowSwapMediaDialog](iprogressui--showswapmediadialog-method.md) | Displays message box to prompt a user to swap media. |
| [IProgressUI::ShowTSProgress](iprogressui--showtsprogress-method.md) | Displays custom task sequence progress information in a dialog box. |

## Remarks

The GUID for `IProgressUI` is B64D758A-01C2-4bf0-9F17-621EFB9CF697.

## See also

- [OS deployment client COM automation classes](operating-system-deployment-client-com-automation-classes.md)
- [ProgressUI Class](progressui-client-com-automation-class.md)
- [About reporting Configuration Manager custom action progress](../../../../osd/about-reporting-configuration-manager-custom-action-progress.md)
