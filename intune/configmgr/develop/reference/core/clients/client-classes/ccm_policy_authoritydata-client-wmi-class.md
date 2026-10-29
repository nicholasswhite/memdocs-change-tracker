---
title: "CCM_Policy_AuthorityData Client WMI Class"
ms.date: "2016-09-20T00:00:00Z"
description: In Configuration Manager, the CCM_Policy_AuthorityData class is a client WMI class that stores information about policy from a particular authority.
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

# CCM_Policy_AuthorityData Client WMI Class

In Configuration Manager, the `CCM_Policy_AuthorityData` class is a client Windows Management Instrumentation (WMI) class that stores information about policy from a particular authority.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class CCM_Policy_AuthorityData : CCM_Policy_Config
{
      DateTime LastReplyTime;
      String Name;
      String ServerCookie;
};
```

## Methods

The `CCM_Policy_AuthorityData` class does not define any methods.

## Properties

`LastReplyTime` Data type: `DateTime`

Access type: Read/Write

Qualifiers: None

The last date and time when the authority replied to a request for policy assignments. If this value is older than the value of `PolicyTimeUntilAck` in the authority's [CCM_PolicyAgent_Configuration Client WMI Class](ccm_policyagent_configuration-client-wmi-class.md) object, the policy requests an acknowledgment. If the value is older than the value of `PolicyTimeUntilExpire`, the policy is expired.

`Name` Data type: `String`

Access type: Read/Write

Qualifiers: [key]

Name of the authority to which the data applies.

`ServerCookie` Data type: `String`

Access type: Read/Write

Qualifiers: None

The last `ServerCookie` value received from the authority in a `ReplyAssignments` message.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Client Runtime Requirements](../../../../core/reqs/client-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Client Development Requirements](../../../../core/reqs/client-development-requirements.md).

## See Also

[Policy Agent Client WMI Classes](policy-agent-client-wmi-classes.md) [CCM_PolicyAgent_Configuration Client WMI Class](ccm_policyagent_configuration-client-wmi-class.md)
