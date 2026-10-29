---
title: "ActivateHierarchy Method in Class SMS_MigrationSiteMapping"
description: The technical details of the ActivateHierarchy method in the SMS_MigrationSiteMapping WMI class.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# ActivateHierarchy Method in Class SMS_MigrationSiteMapping

The `ActivateHierarchy` WMI class method in Configuration Manager activates the hierarchy.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
SInt32 ActivateHierarchy (  
     String sourceSite,  
     String wmiAccount,  
     String sqlAccount,  
     String destinationSiteCode,  
     String scheduleToken  
);  
```

#### Parameters

`sourceSite`  
 Data type: `String` Array

Qualifiers: [in]

The source site FQDN, netBIOS name or IP address.

`wmiAccount`  
 Data type: `String` Array

Qualifiers: `[in]`

The account name to access the WMI provider on the source site.

`sqlAccount`  
 Data type: `String` Array

Qualifiers: [in]

The account name to access SQL Server on the source site.

`destinationSiteCode`  
 Data type: `String` Array

Qualifiers: `[in]`

The destination site's site code. This should be the top site.

`scheduleToken`  
 Data type: `String` Array

Qualifiers: [in]

The schedule for the data gathering job.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../../core/understand/about-configuration-manager-errors.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../core/reqs/server-development-requirements.md).

## See also

[SMS_MigrationEntity Server WMI Class](sms_migrationentity-server-wmi-class.md)
