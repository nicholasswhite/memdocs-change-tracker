---
title: "IProgressUI::CloseProgressDialog method"
description: "IProgressUI::CloseProgressDialog method"
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

# IProgressUI::CloseProgressDialog method

In Configuration Manager, the `CloseProgressDialog` method closes open instances of `IProgressUI`.

## Syntax

```
[IDL]
HRESULT CloseProgressDialog();
```

## Parameters

None

## Return values

An `HRESULT` code. Possible values include, but aren't limited to, the following value. There are no `HRESULT` values returned that are specific to this method.

S_OK The method succeeded.

## See also

- [OS deployment client COM automation classes](operating-system-deployment-client-com-automation-classes.md)
- [IProgressUI interface](iprogressui-interface.md)
- [About reporting Configuration Manager custom action progress](../../../../osd/about-reporting-configuration-manager-custom-action-progress.md)
- [How to use task sequence variables in a running Configuration Manager task sequence](../../../../osd/how-to-use-task-sequence-variables-in-a-running-task-sequence.md)
