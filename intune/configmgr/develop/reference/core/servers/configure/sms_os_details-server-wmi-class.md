---
title: "SMS_OS_Details Server WMI Class"
description: An SMS Provider server class that describes the supported platforms, such as, operating system, architecture, and versions, on which a program can run.
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

# SMS_OS_Details Server WMI Class

The `SMS_OS_Details` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that describes the supported platforms (operating system, architecture, and versions) on which a program can run.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_OS_Details
{
      String MaxVersion;
      String MinVersion;
      String Name;
      String Platform;
};
```

## Methods

The `SMS_OS_Details` class doesn't define any methods.

## Properties

`MaxVersion` Data type: `String`

Access type: Read/Write

Qualifiers: None

The maximum operating system version of the range that is described by this class. The default value is "".

`MinVersion` Data type: `String`

Access type: Read/Write

Qualifiers: None

The minimum operating system version of the range described by this class. The default value is "".

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: None

The name of the operating system. The default value is "".

`Platform` Data type: `String`

Access type: Read/Write

Qualifiers: None

The hardware platform on which the operating system runs.

## Remarks

Class qualifiers for this class include:

- Embedded

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

  The values you specify in this class must come from the [SMS_SupportedPlatforms Server WMI Class](sms_supportedplatforms-server-wmi-class.md) class.

## Requirements

### Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).

## See Also

[SMS_Program Server WMI Class](sms_program-server-wmi-class.md) [How to Modify the Supported Platforms for a Program](../../../../core/servers/configure/how-to-modify-the-supported-platforms-for-a-program.md)
