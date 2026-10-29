---
title: "SMS_CategoryInstance Server WMI Class"
description: An SMS Provider server class that represents a category instance for replicating information about a category, for example, a product or a classification, to all child sites.
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

# SMS_CategoryInstance Server WMI Class

The `SMS_CategoryInstance` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents a category instance used to replicate information about a category, for example, a product or a classification, to all child sites. This class is used in settings management monitoring.

## Syntax

```
Class SMS_CategoryInstance : SMS_CategoryInstanceBase
{
      String CategoryInstance_UniqueID;
      UInt32 CategoryInstanceID;
      String CategoryTypeName;
      String LocalizedCategoryInstanceName;
      SMS_Category_LocalizedProperties LocalizedInformation[];
      UInt32 LocalizedPropertyLocaleID;
      UInt32 ParentCategoryInstanceID;
      String SourceSite;
};
```

## Methods

The `SMS_CategoryInstance` class does not define any methods.

## Properties

`CategoryInstance_UniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: [unique, SizeLimit("512")

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`CategoryInstanceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`CategoryTypeName` Data type: `String`

Access type: Read/Write

Qualifiers: None

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`LocalizedCategoryInstanceName` Data type: `String`

Access type: Read-only

Qualifiers: [read]

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`LocalizedInformation` Data type: `SMS_Category_LocalizedProperties` Array

Access type: Read/Write

Qualifiers: [lazy]

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`LocalizedPropertyLocaleID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`ParentCategoryInstanceID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [read]

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

`SourceSite` Data type: `String`

Access type: Read-only

Qualifiers: [read]

See [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md).

## Remarks

Class qualifiers for this class include:

- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

  To use this class, the application creates an `SMS_CategoryInstance` object and sets the properties, as required, for the particular baseline configuration item.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Compliance Settings (DCM) Server WMI Classes](compliance-settings-dcm-server-wmi-classes.md) [SMS_CategoryInstanceBase Server WMI Class](sms_categoryinstancebase-server-wmi-class.md) [SMS_BaselineAssignment Server WMI Class](sms_baselineassignment-server-wmi-class.md) [SMS_ConfigurationBaselineInfo Server WMI Class](sms_configurationbaselineinfo-server-wmi-class.md)
