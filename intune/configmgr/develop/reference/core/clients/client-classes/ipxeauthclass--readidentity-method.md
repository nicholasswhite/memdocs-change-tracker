---
description: Learn how to use the Configuration Manager with the CreateIdentity method to create a PXE certificate identity that is used in the client configuration file.
title: "IPxeAuthClass::ReadIdentity Method"
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

# IPxeAuthClass::ReadIdentity Method

In Configuration Manager, the `ReadIdentity` method reads a PXE certificate identity from the client configuration (PFX) file. The method is used in serializing a certificate from the file.

## Syntax

```
HRESULT ReadIdentity(
   BSTR FileName,
   BSTR FilePassword,
   BSTR SMSID,
   VARIANT* Identity
);
```

#### Parameters

`FileName` Data type: `BSTR`

Qualifiers: [in]

Name of the client configuration (PFX) file.

`FilePassword` Data type: `BSTR`

Qualifiers: [in]

Password to use for access to the client configuration file.

`SMSID` Data type: `BSTR`

Qualifiers: [in]

The GUID used to identify the certificate. This is the value of the SMSID property in [SMS_CertificateInfo Server WMI Class](../../../osd/sms_certificateinfo-server-wmi-class.md).

`Identity` Data type: `VARIANT`

Qualifiers: [out, retval]

PXE certificate identity. The return value can be used with [SubmitRegistrationRecord Method in Class SMS_Site](../../servers/configure/submitregistrationrecord-method-in-class-sms_site.md).

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following value.

S_OK The method succeeded.

## Remarks

## See Also

[IPxeAuthClass Interface](ipxeauthclass-interface.md) [About Operating System Deployment Site Role Configuration](../../../../osd/about-operating-system-deployment-site-role-configuration.md)
