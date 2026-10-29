---
description: Learn how to represent a device connected to the ActiveSyn service using SMS_ActiveSyncConnectedDevice class.
title: "SMS_ActiveSyncConnectedDevice Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_ActiveSyncConnectedDevice Client WMI Class

The `SMS_ActiveSyncConnectedDevice` class is a client Windows Management Instrumentation (WMI) class, in Configuration Manager, that represents a device connected to the ActiveSync service.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ActiveSyncConnectedDevice : SMS_Class_Template
{
      String DeviceOEMInfo;
      String DeviceType;
      String InstalledClientID;
      String InstalledClientServer;
      String InstalledClientVersion;
      String LastSyncTime;
      String OS_AdditionalInfo;
      String OS_Build;
      String OS_Major;
      String OS_Minor;
      String OS_Platform;
      String ProcessorArchitecture;
      String ProcessorLevel;
      String ProcessorRevision;
};
```

## Methods

The `SMS_ActiveSyncConnectedDevice` class does not define any methods.

## Properties

`DeviceOEMInfo` Data type: `String`

Access type: Read/Write

Qualifiers:

[SMS_Report("True"), key]

OEM information for the device.

`DeviceType` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True"), key]

Type of device.

`InstalledClientID` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True")]

The ID of the installed client.

`InstalledClientServer` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True")]

The ID of the server for the installed client.

`InstalledClientVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True")]

The version of the installed client.

`LastSyncTime` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True")]

The time when the device was last synchronized.

`OS_AdditionalInfo` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True")]

Additional information about the client operating system.

`OS_Build` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True")]

The build associated with the client operating system.

`OS_Major` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True"), key]

The major version number of the operating system.

`OS_Minor` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True"), key]

The minor version number of the operating system.

`OS_Platform` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True"), key]

The platform on which the operating system is running.

`ProcessorArchitecture` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True"), key]

The architecture for the device processor.

`ProcessorLevel` Data type: `String`

Access type: Read/Write

Qualifiers: SMS_Report("True"), key]

The processor level.

`ProcessorRevision` Data type: `String`

Access type: Read/Write

Qualifiers: [SMS_Report("True"), key]

The processor revision.

## Remarks

All properties of this class are marked with qualifiers to indicate that they represent items that are generated dynamically (reported) based on the content of the SMS_def.mof file.

## See Also

[Device Management Client WMI Classes](device-management-client-wmi-classes.md) [SMS_ActiveSyncService Client WMI Class](sms_activesyncservice-client-wmi-class.md)
