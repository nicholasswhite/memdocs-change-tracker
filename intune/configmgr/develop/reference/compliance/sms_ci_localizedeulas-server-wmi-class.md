---
title: "SMS_CI_LocalizedEulas Server WMI Class"
description: An SMS Provider server class in Configuration Manager. It contains the localized Microsoft Software License Terms information for a configuration item.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/fcc3cd4a-59ea-47a2-9cc1-784142a5a25d
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/24dc3ccd-591a-4415-a1fe-8759afafcb12
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_CI_LocalizedEulas Server WMI Class

The `SMS_CI_LocalizedEulas` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that contains the localized Microsoft Software License Terms information for a configuration item.

## Syntax

```
Class SMS_CI_LocalizedEulas
{
      String EULAContentUniqueID;
      UInt32 LocaleID;
};
```

## Methods

The `SMS_CI_LocalizedEulas` class does not define any methods.

## Properties

`EULAContentUniqueID` Data type: `String`

Access type: `Read/Write`

Qualifiers: `None`

Unique ID of the Microsoft Software License Terms content.

`LocaleID` Data type: `UInt32`

Access type: `Read/Write`

Qualifiers: `None`

The ID of the locale associated with the localized information.

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  This class is embedded by the following classes, through the `LocalizedEulas` property:
- [SMS_ConfigurationItem Server WMI Class](sms_configurationitem-server-wmi-class.md)
- [SMS_Driver Server WMI Class](../osd/sms_driver-server-wmi-class.md)
- [SMS_SoftwareUpdate Server WMI Class](../sum/sms_softwareupdate-server-wmi-class.md)

  Your application uses this class only if the `EULAExists` property of the configuration item is set to `true`.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Compliance Settings (DCM) Server WMI Classes](compliance-settings-dcm-server-wmi-classes.md) [SMS_ConfigurationItem Server WMI Class](sms_configurationitem-server-wmi-class.md)
