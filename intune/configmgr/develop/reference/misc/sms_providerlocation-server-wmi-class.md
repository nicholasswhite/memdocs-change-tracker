---
title: "SMS_ProviderLocation Server WMI Class"
description: The SMS_ProviderLocation Windows Management Instrumentation (WMI) class, in Configuration Manager, identifies the location of the SMS Provider for a site.
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

# SMS_ProviderLocation Server WMI Class

The `SMS_ProviderLocation` Windows Management Instrumentation (WMI) class, in Configuration Manager, identifies the location of the SMS Provider for a site.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ProviderLocation
{
     String Machine;
     String NamespacePath;
     Boolean ProviderForLocalSite;
     String SiteCode;
};
```

## Properties

`Machine` Data type: `String`

Access type: Read/Write

Qualifiers: None

Name of the computer on which the SMS Provider resides.

`NamespacePath` Data type: `String`

Access type: Read/Write

Qualifiers: None

Full WMI path to the SMS Provider namespace.

`ProviderForLocalSite` Data type: `Boolean`

Access type: Read/Write

Qualifiers: None

`true` if the SMS Provider is set as the local site server for the client.

`SiteCode` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Site code of the site.

## Remarks

There are no special class qualifiers for this class. For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](class-and-property-qualifiers.md).

For information on using this class, see [How to Connect to an SMS Provider in Configuration Manager by Using WMI](../../core/understand/how-to-connect-to-an-sms-provider-in-configuration-manager-by-using-wmi.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).
