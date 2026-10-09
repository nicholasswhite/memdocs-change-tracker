---
description: Learn how to use the IsUsedCert method to verify whether the specified certificate is used.
title: "IsUsedCert Method in Class SMS_Site"
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

# IsUsedCert Method in Class SMS_Site

The `IsUsedCert` Windows Management Instrumentation (WMI) class method, in Configuration Manager, verifies whether the specified certificate is used.

The following syntax is simplified from Managed Object Format (MOF) code and defines the method.

## Syntax

```
Boolean IsUsedCert(
   String Certificate
);
```

#### Parameters

`Certificate` Data type: `String`

Qualifiers: [in]

The certificate to check against the site.

## Return Values

`true` if the specified certificate is used on the site; otherwise `false`.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Site Server WMI Class](sms_site-server-wmi-class.md) [GetClientInfo Method in Class SMS_Site](getclientinfo-method-in-class-sms_site.md)
