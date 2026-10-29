---
title: "SMS_Authority Client WMI Class"
description: In Configuration Manager, the SMS_Authority class is a client Windows Management Instrumentation class that represents the Configuration Manager site that manages the client.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/43b2e5aa-8a6d-4de2-a252-692232e5edc8
- https://authoring-docs-microsoft.poolparty.biz/devrel/d7a55faf-a992-4e27-aa3a-eadc9830e778
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# SMS_Authority Client WMI Class

The `SMS_Authority` class is a client Windows Management Instrumentation (WMI) class, in Configuration Manager, that represents the Configuration Manager site that manages the client.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_Authority : CCM_Authority
{
      String Capabilities;
      String CurrentManagementPoint;
      UInt32 Index;
      String Name;
      UInt32 PolicyOrder;
      String PolicyRequestTarget;
      String Protocol;
      String SigningCertificate;
      UInt32 Version;
};
```

## Methods

The `SMS_Authority` class does not define any methods.

## Properties

`Capabilities` Data type: `String`

Access type: Read/Write

Qualifiers: None

Reserved.

`CurrentManagementPoint` Data type: `String`

Access type: Read/Write

Qualifiers: None

The current management point for the site.

`Index` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

For assigned Management Point rotation.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Name of the authority.

`PolicyOrder` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

Determines the priority of the authority when resolving policy conflicts. The lower the order, the higher the priority of the authority's policy.

`PolicyRequestTarget` Data type: `String`

Access type: Read/Write

Qualifiers: None

Specifies the target for requesting policy assignments. If this value is NULL, no policy is requested for this authority.

`Protocol` Data type: `String`

Access type: Read/Write

Qualifiers: None

Reserved.

`SigningCertificate` Data type: `String`

Access type: Read/Write

Qualifiers: None

The site signing certificate. This is only relevant in native mode.

`Version` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

The version of the authority.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md)
