---
title: "SMS_WSfBConfigurationData Server WMI Class"
description: An SMS Provider server class, in Configuration Manager, that represents Microsoft Store for Business configuration data.
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

# SMS_WSfBConfigurationData Server WMI Class

The `SMS_WSfBConfigurationData` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents Microsoft Store for Business configuration data.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_WSfBConfigurationData : SMS_BaseClass
{
    String ClientId;
    String ContentLocation;
    String DefaultLocale;
    DateTime LastSuccessfulSyncTime;
    SInt32 LastSyncStatus;
    DateTime LastSyncTime;
    String SelectedLocales;
    String TenantId;
};

```

## Methods

The `SMS_WSfBConfigurationData` class does not define any methods.

## Properties

`ClientId` Data type: `String`

Access type: Read

Qualifiers: none

Microsoft Store For Business client ID.

`ContentLocation` Data type: `String`

Access type: Read

Qualifiers: none

Location of the content downloaded from the Microsoft Store For Business.

`DefaultLocale` Data type: `String`

Access type: Read

Qualifiers: none

The default language for the Microsoft Store for Business.

`LastSuccessfulSyncTime` Data type: `DateTime`

Access type: Read

Qualifiers: none

The time of the last successful synchronization with Microsoft Store for Business.

`LastSyncStatus` Data type: `SInt32`

Access type: Read

Qualifiers: none

The status of the last synchronization with Microsoft Store for Business.

`LastSyncTime` Data type: `DateTime`

Access type: Read

Qualifiers: none

The time of the last synchronization with Microsoft Store for Business.

`SelectedLocales` Data type: `String`

Access type: Read

Qualifiers: none

The selected languages for Microsoft Store for Business.

`TenantId` Data type: `String`

Access type: Read

Qualifiers: [key]

Microsoft Store for Business tenant ID.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Read (read-only)
- Secured

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../misc/class-and-property-qualifiers.md).

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../core/reqs/server-development-requirements.md).

## See Also

[Configuration Manager Compliance Settings (DCM) Server WMI Classes](compliance-settings-dcm-server-wmi-classes.md)
