---
title: "SMS_G_System_AdvancedThreatProtectionHealthStatus Server WMI Class"
ms.date: "2019-05-13T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
description: An overview of SMS_G_System_AdvancedThreatProtectionHealthStatus Server WMI Class
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/8b9ae643-2e85-42b8-beb2-eef4bae8c4bc
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/e047e27d-b5f3-43a8-b4b0-4f6dca95e7c9
---

# SMS_G_System_AdvancedThreatProtectionHealthStatus Server WMI Class

The `SMS_G_System_AdvancedThreatProtectionHealthStatus` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that represents Microsoft Defender for Endpoint client health status.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_G_System_AdvancedThreatProtectionHealthStatus : SMS_G_System
{
    DateTime LastConnected;
    UInt32 OnboardingState;
    String OrgId;
    UInt32 ResourceID;
    Boolean SenseIsRunning;
};
```

## Methods

The `SMS_G_System_AdvancedThreatProtectionHealthStatus` class does not define any methods.

## Properties

`LastConnected` Data type: `DateTime`

Access type: Read

Qualifiers: [not_null]

The time that the Microsoft Defender for Endpoint agent last connected to the cloud.

`OnboardingState` Data type: `UInt32`

Access type: Read

Qualifiers: [not_null]

The onboarding state.

`OrgId` Data type: `String`

Access type: Read

Qualifiers: [not_null]

The ID of the organization that the Microsoft Defender for Endpoint agent reports to.

`ResourceID` Data type: `UInt32`

Access type: Read

Qualifiers: [key, not_null]

See [SMS_G_System Server WMI Class](sms_g_system-server-wmi-class.md).

`SenseIsRunning` Data type: `Boolean`

Access type: Read

Qualifiers: [not_null]

Indicates whether the Microsoft Defender for Endpoint agent is running.

## Remarks

Class qualifiers for this class include:

- Dynamic
- Secured
- Read (read-only)

  For more information about both the class qualifiers and the property qualifiers included in the Properties section, see [Configuration Manager Class and Property Qualifiers](../../../misc/class-and-property-qualifiers.md).

## Requirements

### Runtime requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

### Development requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
