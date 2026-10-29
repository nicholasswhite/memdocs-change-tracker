---
description: Learn how to define a media certificate that is registered by Configuration Manager and used by PXE clients to communicate with a management point.
title: "SMS_PXECertificateInfo Server WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_PXECertificateInfo Server WMI Class

The `SMS_PXECertificateInfo` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that defines a media certificate that is registered by Configuration Manager and used by PXE clients to communicate with a management point.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_PXECertificateInfo : SMS_CertificateInfo
{
      String Certificate;
      Boolean IsApproved;
      Boolean IsBlocked;
      String IssuedTo;
      SInt32 KeyType;
      String PublicKey;
      String PXEServerName;
      String SMSID;
      String Thumbprint;
      UInt32 Type;
      DateTime ValidFrom;
      DateTime ValidUntil;
};
```

## Methods

The `SMS_PXECertificateInfo` class does not define any methods.

## Properties

`Certificate` Data type: `String`

Access type: Read/Write

Qualifiers: [large, lazy]

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`IsApproved` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`IsBlocked` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`IssuedTo` Data type: `String`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`KeyType` Data type: `SInt32`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`PublicKey` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy]

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`PXEServerName` Data type: `String`

Access type: Read/Write

Qualifiers: None

The name of the PXE server to which the PXE certificate belongs.

`SMSID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`Thumbprint` Data type: `String`

Access type: Read/Write

Qualifiers: [Lazy]

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`Type` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`ValidFrom` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

`ValidUntil` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

See [SMS_CertificateInfo Server WMI Class](sms_certificateinfo-server-wmi-class.md).

## Remarks

Class qualifiers for this class include:

- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See also

[SMS_CertificateInfo server WMI class](sms_certificateinfo-server-wmi-class.md)
