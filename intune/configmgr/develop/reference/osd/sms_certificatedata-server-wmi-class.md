---
description: Learn how to represent certificate data managed by Configuration Manager using SMS_CertificateData class.
title: "SMS_CertificateData Server WMI Class"
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

# SMS_CertificateData Server WMI Class

The `SMS_CertificateData` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents certificate data managed by Configuration Manager.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CertificateData : SMS_BaseClass
{
    String CertID;
    UInt32 CertType;
    String Description;
    String Name;
};
```

## Methods

The following table lists the methods in the `SMS_CertificateData` class.

| Method | Description |
| --- | --- |
| [SubmitCertificate Method in Class SMS_CertificateData](submitcertificate-method-in-class-sms_certificatedata.md) | Submit certificate. |
| [DeleteCertificate Method in Class SMS_CertificateData](deletecertificate-method-in-class-sms_certificatedata.md) | Deletes the certificate from the database. |

## Properties

`CertID` Data type: `String`

Access type: Read-only

Qualifiers: [key, read]

Certificate unique identifier.

`CertType` Data type: `UInt32`

Access type: Read-only

Qualifiers: [enumeration, read]

Certificate type. Possible values are:

| Value | Certificate type |
| --- | --- |
| 1 | Windows Intune Subscription |

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: none

Certificate description.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: none

Certificate name.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
