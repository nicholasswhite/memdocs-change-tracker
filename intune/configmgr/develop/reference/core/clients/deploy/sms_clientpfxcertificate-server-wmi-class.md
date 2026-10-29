---
title: "SMS_ClientPfxCertificate Server WMI Class"
description: The SMS_ClientPfxCertificate Windows Management Instrumentation class is an SMS Provider server class, in Configuration Manager, that contains an imported  Pfx certificate.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/4c50f262-d533-4ba4-9d4a-08899ec3a3d1
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_ClientPfxCertificate Server WMI Class

The `SMS_ClientPfxCertificate` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that contains an imported Pfx certificate.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ClientPfxCertificate : SMS_BaseClass
{
    UInt32 CI_ID;
    UInt32 DeviceID;
    UInt32 IsTombstoned;
    String ProfileName;
    String Thumbprint;
    UInt32 UserItemKey;
    String UserName;
    DateTime ValidFrom;
    DateTime ValidUntil;
};

```

## Methods

The following table lists the methods in the `SMS_ClientPfxCertificate` class.

| Method | Description |
| --- | --- |
| [ImportForUser Method in Class SMS_ClientPfxCertificate](importforuser-method-in-class-sms_clientpfxcertificate.md) | Imports a certificate for a user, encrypted by using a password. |
| [DeleteForUser Method in Class SMS_ClientPfxCertificate](deleteforuser-method-in-class-sms_clientpfxcertificate.md) | Deletes a certificate for a user. |

## Properties

`CI_ID` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The unique ID of the configuration item.

`DeviceID` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The ID of the device.

`IsTombstoned` Data type: `UInt32`

Access type: Read

Qualifiers: none

Specifies whether the certificate is marked for deletion.

`ProfileName` Data type: `String`

Access type: Read

Qualifiers: [key]

An SMS_ConfigurationPolicy Profile unique ID.

`Thumbprint` Data type: `String`

Access type: Read

Qualifiers: [key]

The thumbprint for the certificate.

`UserItemKey` Data type: `UInt32`

Access type: Read

Qualifiers: [key]

The user item key.

`UserName` Data type: `String`

Access type: Read

Qualifiers: [key]

The user name.

`ValidFrom` Data type: `DateTime`

Access type: Read

Qualifiers: none

The start date for the certificate.

`ValidUntil` Data type: `DateTime`

Access type: Read

Qualifiers: none

The expiration date for the certificate.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
