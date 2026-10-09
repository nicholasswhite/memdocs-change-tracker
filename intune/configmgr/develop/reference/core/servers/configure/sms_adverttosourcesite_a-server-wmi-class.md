---
description: Learn how to relate an SMS Advertisement Server class object with the SMS Site Server class object that created the advertisement.
title: "SMS_AdvertToSourceSite_a Server WMI Class"
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

# SMS_AdvertToSourceSite_a Server WMI Class

The `SMS_AdvertToSourceSite_a` association Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that relates an [SMS_Advertisement Server WMI Class](sms_advertisement-server-wmi-class.md) object with the [SMS_Site Server WMI Class](sms_site-server-wmi-class.md) object that created the advertisement.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_AdvertToSourceSite_a : SMS_BaseAssociation
{
   ref:SMS_Site advertSourceSite;
      ref:SMS_Advertisement ownedAdvert;
};
```

## Methods

The `SMS_AdvertToSourceSite_a` class does not define any methods.

## Properties

`advertSourceSite` Data type: `ref:MS_Site`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_Site Server WMI Class](sms_site-server-wmi-class.md) object path.

`ownedAdvert` Data type: `ref:SMS_Advertisement`

Access type: Read/Write

Qualifiers: [key]

Reference to an [SMS_Advertisement Server WMI Class](sms_advertisement-server-wmi-class.md) object path.

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

## See Also

[SMS_Site Server WMI Class](sms_site-server-wmi-class.md) [SMS_Advertisement Server WMI Class](sms_advertisement-server-wmi-class.md)
