---
title: "IProgressUI::ShowTSProgress method"
description: "IProgressUI::ShowTSProgress method"
ms.date: "2019-04-03T00:00:00Z"
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

# IProgressUI::ShowTSProgress method

In Configuration Manager, the `ShowTSProgress` method displays custom task sequence progress information in a dialog box.

## Syntax

```
[IDL]
HRESULT ShowActionProgress(
     BSTR pszOrgName,
     BSTR pszTaskSequenceName,
     BSTR pszCustomTitle,
     BSTR pszCurrentAction,
     ULONG uStep,
     ULONG uMaxStep,
);
```

### Parameters

#### `pszOrgName`

Data type: `BSTR`

Qualifiers: [in]

Pointer to the organization name that is shown in the progress dialog box. The value can be retrieved from the `_SMSTSOrgName` environment variable.

#### `pszTaskSequenceName`

Data type: `BSTR`

Qualifiers: [in]

Pointer to the name of the task sequence that is currently running. The value can be retrieved from the `_SMSTSPackageName` environment variable.

#### `pszCustomTitle`

Data type: `BSTR`

Qualifiers: [in]

Pointer to the text for a custom message that replaces the default title text displayed in the progress dialog box. Pass an empty string if there's no custom message to show. The value can be obtained from the `_SMSTSCustomProgressDialogMessage` environment variable.

#### `pszCurrentAction`

Data type: `BSTR`

Qualifiers: [in]

Pointer to the name of the current task sequence step. The value can be obtained from the `_SMSTSCurrentActionName` environment variable.

#### `uStep`

Data type: `ULONG`

Qualifiers: [in]

The current task sequence step number. The value can be obtained from the `SMSTSNextInstructionPointer` environment variable.

#### `uMaxStep`

Data type: `ULONG`

Qualifiers: [in]

The total number of steps in the task sequence. The value can be obtained from the `_SMSTSInstructionTableSize` environment variable.

## Return values

An `HRESULT` code. Possible values include, but aren't limited to, the following value. There are no `HRESULT` values returned that are specific to this method.

S_OK The method succeeded.

## See also

- [OS deployment client COM automation classes](operating-system-deployment-client-com-automation-classes.md)
- [IProgressUI interface](iprogressui-interface.md)
- [About reporting Configuration Manager custom action progress](../../../../osd/about-reporting-configuration-manager-custom-action-progress.md)
- [How to use task sequence variables in a running Configuration Manager task sequence](../../../../osd/how-to-use-task-sequence-variables-in-a-running-task-sequence.md)
