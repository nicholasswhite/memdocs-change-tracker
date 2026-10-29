---
title: "SMS_DeviceSettingItem Server WMI Class"
description: The SMS_DeviceSettingItem WMI class provides the functionality to create a device setting configuration item in the database.
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

# SMS_DeviceSettingItem Server WMI Class

The `SMS_DeviceSettingItem` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that provides the functionality to create a device setting configuration item in the database.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_DeviceSettingItem : SMS_BaseClass
{
    String Description;
    String DeviceSettingItemUniqueID;
    String Name;
    String PropList;
    String SourceSite;
    String Type;
    UInt32 Version;
};
```

## Methods

The `SMS_DeviceSettingItem` class does not define any methods.

## Properties

`Description` Data type: `String`

Access type: Read/Write

Qualifiers: None

Description of the device setting to create. The default value is "".

`DeviceSettingItemUniqueID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

A GUID or unique ID that identifies the device setting item to create. The default value is "".

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [unique]

Name of the device setting item to create. The default value is "".

`PropList` Data type: `String`

Access type: Read/Write

Qualifiers: [lazy]

A list of properties for the device setting item.

`SourceSite` Data type: `String`

Access type: Read/Write

Qualifiers: None

The site code of the site for which to create the device setting item. The default value is "".

`Type` Data type: `String`

Access type: Read/Write

Qualifiers: None

Type of device setting item. The default value is "".

`Version` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The version of the device setting item. The default value is 1.

## Remarks

Class qualifiers for this class include:

- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Device Management Server WMI Classes](device-management-server-wmi-classes.md)
