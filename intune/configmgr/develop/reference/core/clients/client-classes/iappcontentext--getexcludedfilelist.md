---
description: "Learn how to get the excluded file list for application content used to support selective file download with IAppContentExt::GetExcludedFileList method."
title: "IAppContentExt::GetExcludedFileList"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
manager: laurawi
moniker_range_name: ''
ms.author: dannygu
ms.reviewer:
- brianhun
- hugowu
- payur
- qiani
- umaikhan
cmProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/a72e95ff-4b4f-4cc1-90c6-7dcba67ff05f
spProducts:
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# IAppContentExt::GetExcludedFileList

The `IAppContentExt::GetExcludedFileList` method, in Configuration Manager, gets the excluded file list for application content. This is used to support selective file download.

## Syntax

```
[IDL]
HRESULT GetExcludedFileList(
     IWbemClassObject* pHandlerSynclet,
     LPWSTR* pwszExcludedFileList,
     BOOL* pbForceFileExclusion
);
```

#### Parameters

`*pHandlerSynclet` Data type: `IWbemClassObject`

Qualifiers: [in]

.

`pwszExcludedFileList` Data type: `LPWSTR`

Qualifiers: [out]

The exclude file list is a single string separated by the ':' character. For example, "File1.txt:File2.exe."

`pbForceFileExclusion` Data type: `BOOL`

Qualifiers: [out]

`True` to force exclusion of files. If `False`, content framework decides whether or not excluding them based on network condition and content configuration.

## Return Values

An `HRESULT` code. Possible values include, but aren't limited to, the following one:

S_OK Discovery was triggered successfully. All other return values indicate failure.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Microsoft.ConfigurationManagement.ApplicationManagement](https://learn.microsoft.com/en-us/previous-versions/)] [Configuration Manager Software Development Kit](../../../../core/misc/system-center-configuration-manager-sdk.md) [Configuration Manager Reference](../../../configuration-manager-reference.md)
