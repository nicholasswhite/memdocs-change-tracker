---
title: "SMS_CollectionToPkgAdvert_a Server WMI Class"
description: In Configuration Manager, the SMS_CollectionToPkgAdvert_a association WMI class is an SMS Provider server class that uses the CollectionID property to relate an SMS_Advertisement Server WMI Class object with its target SMS_Collection Server WMI Class object.
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

# SMS_CollectionToPkgAdvert_a Server WMI Class

The `SMS_CollectionToPkgAdvert_a` association Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that uses the `CollectionID` property to relate an [SMS_Advertisement Server WMI Class](../../servers/configure/sms_advertisement-server-wmi-class.md) object with its target [SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) object.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_CollectionToPkgAdvert_a : SMS_BaseAssociation
{
      ref:SMS_Advertisement advert;
      ref:SMS_Collection collection;
};
```

## Methods

The `SMS_CollectionToPkgAdvert_a` class does not define any methods.

## Properties

`advert` Data type: `ref:SMS_Advertisement`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_Advertisement Server WMI Class](../../servers/configure/sms_advertisement-server-wmi-class.md) object path.

`collection` Data type: `ref:SMS_Collection`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_Collection Server WMI Class](sms_collection-server-wmi-class.md) object path.

## Remarks

Class qualifiers for this class include:

- Association: ToInstance
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
