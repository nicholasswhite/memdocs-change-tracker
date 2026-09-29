---
title: "IPxeAuthClass::CreateIdentity Method"
description: Learn how to use the CreateIdentity method to create a new self-signed certificate.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
---

# IPxeAuthClass::CreateIdentity Method

In Configuration Manager, the `CreateIdentity` method creates a PXE certificate identity that is used in the client configuration file. This method is used to create a new self-signed certificate.

## Syntax

```
HRESULT CreateIdentity(
      BSTR FriendlyName,
      BSTR SubjectName,
      BSTR SMSID,
      VARIANT* StartTime,
      VARIANT* EndTime,
      VARIANT* Identity
);
```

#### Parameters

`FriendlyName` Data type: `BSTR`

Qualifiers: [in]

Friendly name of the certificate identity.

`SubjectName` Data type: `BSTR`

Qualifiers: [in]

Name of the certificate subject.

`SMSID` Data type: `BSTR`

Qualifiers: [in]

The GUID used to identify the certificate. This is the value of the SMSID property in [SMS_CertificateInfo Server WMI Class](../../../osd/sms_certificateinfo-server-wmi-class.md).

`StartTime` Data type: `VARIANT`

Qualifiers: [in]

Time when the certificate becomes valid.

`EndTime` Data type: `VARIANT`

Qualifiers: [in]

Time when the validity of the certificate ends.

`Identity` Data type: `VARIANT`

Qualifiers: [out, retval]

PXE certificate identity. Can be used with [SubmitRegistrationRecord Method in Class SMS_Site](../../servers/configure/submitregistrationrecord-method-in-class-sms_site.md).

## Return Values

An `HRESULT` code. Possible values include, but are not limited to, the following value.

S_OK The method succeeded.

## Remarks

## See Also

[IPxeAuthClass Interface](ipxeauthclass-interface.md) [About Operating System Deployment Site Role Configuration](../../../../osd/about-operating-system-deployment-site-role-configuration.md)
