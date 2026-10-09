---
title: "ImportForProfile Method in Class SMS_MDMBulkEnrollmentPackages"
description: The ImportForProfile Windows Management Instrumentation (WMI) class method, in Configuration Manager, imports an On-Premises Mobile Device Management (MDM) bulk enrollment package for a profile.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
---

# ImportForProfile Method in Class SMS_MDMBulkEnrollmentPackages

The `ImportForProfile` Windows Management Instrumentation (WMI) class method, in Configuration Manager, imports an On-Premises Mobile Device Management (MDM) bulk enrollment package for a profile.

## Syntax

```
sint32 ImportForProfile(
     String ProfileGUID,
     String CertificateGUID,
     String PackageName,
     String Certificate
);

```

#### Parameters

`ProfileGUID` Data type: `String`

Qualifiers: [in]

The GUID of the profile.

`CertificateGUID` Data type: `String`

Qualifiers: [in]

The GUID of the certificate.

`PackageName` Data type: `String`

Qualifiers: [in]

Package name.

`Certificate` Data type: `String`

Qualifiers: [in]

The root certificate.

## Return Values

An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.

For more information about handling returned errors, see [About Configuration Manager Errors](../../core/understand/about-configuration-manager-errors.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[SMS_MDMBulkEnrollmentPackages Server WMI Class](sms_mdmbulkenrollmentpackages-server-wmi-class.md)
