---
description: Learn how to use the GetSiteADInfo method to get Active Directory information of the site server.
title: "GetSiteADInfo Method in Class SMS_Site"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/b1cfdec6-b0c3-4209-818c-736879856e0e
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/37da4cc9-0cfc-42a9-ba5e-805706b01ef8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/2d0723c1-cf38-4c30-ab3d-5df787b33270
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/3661fb96-d414-4a4e-b7ad-9370637790dd
---

# GetSiteADInfo Method in Class SMS_Site

The `GetSiteADInfo` Windows Management Instrumentation (WMI) class method, in Configuration Manager, gets Active Directory information of site server.

The following syntax is simplified from Managed Object Format (MOF) code and is intended to show the definition of the method.

## Syntax

```
SInt32 GetSiteADInfo(
   String SiteCode,
   String DCName,
   String DCAddress,
   String DomainName,
   String ForestName,
   String DCSiteName,
   String ClientSiteName
);
```

#### Parameters

`SiteCode` Data type: `String`

Qualifiers: [in]

Site code.

`DCName` Data type: `String`

Qualifiers: [out]

Name of the Active Directory domain controller.

`DCAddress` Data type: `String`

Qualifiers: [out]

Domain controller address.

`DomainName` Data type: `String`

Qualifiers: [out]

Domain name.

`ForestName` Data type: `String`

Qualifiers: [out]

Name of the Active Directory forest.

`DCSiteName` Data type: `String`

Qualifiers: [out]

Name of the Active Directory site where the domain controller is located.

`ClientSiteName` Data type: `String`

Qualifiers: [out]

Name of the site that the computer belongs to.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For information about handling returned errors, see [About Configuration Manager Errors](../../../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Identification Server WMI Class](sms_identification-server-wmi-class.md)
