---
title: "SMS_SCFToSCI_a Server WMI Class"
description: The SMS_SCFToSCI_a Windows Management Instrumentation class is an SMS Provider server class, in Configuration Manager, that relates a WMI class object.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_SCFToSCI_a Server WMI Class

The `SMS_SCFToSCI_a` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that relates an [SMS_SiteControlFile Server WMI Class](sms_sitecontrolfile-server-wmi-class.md) object with [SMS_SiteControlItem Server WMI Class](sms_sitecontrolitem-server-wmi-class.md) objects that make up the current site control file.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_SCFToSCI_a : SMS_BaseAssociation
{
      ref:SMS_SiteControlFile SiteControlFile;
      ref:SMS_SiteControlItem SiteControlItem;
};
```

## Properties

`SiteControlFile` Data type: `ref:SMS_SiteControlFile`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_SiteControlFile Server WMI Class](sms_sitecontrolfile-server-wmi-class.md) object path.

`SiteControlItem` Data type: `ref:SMS_SiteControlItem`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_SiteControlItem Server WMI Class](sms_sitecontrolitem-server-wmi-class.md) object path.

## Remarks

Class qualifiers for this class include:

- Association: ToInstance
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Site Configuration Server WMI Classes](site-configuration-server-wmi-classes.md)
