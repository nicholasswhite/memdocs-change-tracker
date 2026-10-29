---
title: "CCM_Service_IISConfiguration Client WMI Class"
description: In Configuration Manager, the CCM_Service_IISConfiguration class is a client Windows Management Instrumentation class that supports Internet Information Services-related settings used by CCMEXEC for staging and receiving message payloads on a Management Point.
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

# CCM_Service_IISConfiguration Client WMI Class

In Configuration Manager, the `CCM_Service_IISConfiguration` class is a client Windows Management Instrumentation (WMI) class that supports Internet Information Services (IIS)-related settings used by CCMEXEC for staging and receiving message payloads on a Management Point.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Service_IISConfiguration : CCM_Policy
{
      UInt8 Dummy[key]  ;
      String IncomingPayloadDir;
      String IncomingPayloadVirtualDir;
      String OutgoingPayloadDir;
      String OutgoingPayloadVirtualDir;
      String PolicyID;
      String PolicyInstanceID;
      UInt32 PolicyPrecedence;
      String PolicyRuleID;
      String PolicySource;
      String PolicyVersion;
};
```

## Methods

The `CCM_Service_IISConfiguration` class does not define any methods.

## Properties

`Dummy[key]` Data type: `UInt8`

Access type: Read/Write

Qualifiers: [Realkey]

Dummy key.

`IncomingPayloadDir` Data type: `String`

Access type: Read/Write

Qualifiers: None

Directory where message payloads are uploaded to the server by clients. The System and Administrators account must have full access to this directory. In addition, the appropriate permissions must be given to allow clients to upload to this directory by means of IIS using the BITS ISAPI component. This directory must be created at install time; it is not automatically created by the service.

`IncomingPayloadVirtualDir` Data type: `String`

Access type: Read/Write

Qualifiers: None

IIS virtual directory mapped to **IncomingPayloadDir**.

`OutgoingPayloadDir` Data type: `String`

Access type: Read/Write

Qualifiers: None

Directory that is used to hold message payloads that will be downloaded by clients.

`OutgoingPayloadVirtualDir` Data type: `String`

Access type: Read/Write

Qualifiers: None

IIS virtual directory mapped to **OutgoingPayloadDir**.

`PolicyID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyInstanceID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyPrecedence` Data type: `UInt32`

Access type: Read/Write

Qualifiers: None

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyRuleID` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicySource` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

`PolicyVersion` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

See [CCM_Policy Client WMI Class](ccm_policy-client-wmi-class.md).

## Remarks

An instance of this class should exist only if IIS has been configured to work with CCMEXEC, that is, IIS must be installed and the appropriate physical and virtual directories must be set up correctly. If this instance is omitted, CCMEXEC operates without using IIS, thus losing some functionality.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Client Framework and Data Transfer Client WMI Classes](client-framework-and-data-transfer-client-wmi-classes.md)
