---
description: Learn how to represent the state information for a single Content Transfer Manager job using CCM_CTM_JobStateEx4 class.
title: CCM_CTM_JobStateEx4 Class
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# CCM_CTM_JobStateEx4 Class

The **CCM_CTM_JobStateEx4** class, in Configuration Manager, represents the state information for a single Content Transfer Manager job.

## Syntax

```
class CCM_CTM_JobStateEx4
{
    string ProviderSettingsFromRequest;
    uint32 CurrentProviderPriority;
    string CurrentProviderLogicalName;
    string CurrentProviderCLSID;
    string CurrentProviderGlobalSettings;
    string CurrentProviderSettingsFromRequest;
};

```

#### Parameters

`ProviderSettingsFromRequest` Data type: String

Qualifiers: [in]

XML describing the allowed alternate providers and provider-specific settings.

`CurrentProviderPriority` Data type: UInt32

Qualifiers: [in]

Priority in the face of multiple alternate provider choices. For future use.

`CurrentProviderLogicalName` Data type: String

Qualifiers: [in]

The name of the current provider. This value must match the value specified to the SMS provider.

`CurrentProviderCLSID` Data type: String

Qualifiers: [in]

The COM class ID corresponding to the current provider.

`CurrentProviderGlobalSettings` Data type: String

Qualifiers: [in]

Provider-specific data for the current provider.

`CurrentProviderSettingsFromRequest` Data type: String

Qualifiers: [in]

Provider-specific settings for the current provider.

## Return Values

None.

## Remarks

There will be an instance of this class for each job started by the Content Transfer Manager.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).
