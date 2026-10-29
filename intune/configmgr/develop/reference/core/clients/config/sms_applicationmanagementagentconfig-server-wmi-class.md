---
title: "SMS_ApplicationManagementAgentConfig Server WMI Class"
description: In Configuration Manager, the SMS_ApplicationManagementAgentConfig WMI class is an SMS Provider server class that contains the configuration of Application Management client agent settings.
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

# SMS_ApplicationManagementAgentConfig Server WMI Class

The `SMS_ApplicationManagementAgentConfig` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that contains the configuration of Application Management client agent settings.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_ApplicationManagementAgentConfig : SMS_ClientAgentConfig_BaseClass
{
    UInt32 AgentID;
    String AlternateContentProviders;
    Boolean AppXInplaceUpgradeEnabled;
    Boolean Enabled;
    String EvaluationSchedule;
};
```

## Methods

The `SMS_ApplicationManagementAgentConfig` class does not define any methods.

## Properties

`AgentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Identifies the client agent component. The Application Management Agent ID is 17.

`AlternateContentProviders` Data type: `String`

Access type: Read/Write

Qualifiers: none

An XML string to set alternate content provider settings. This property does not apply to a software update package or a driver package.

```
<AlternateDownloadSettings SchemaVersion="1.0">    <Provider Name="logical name here">        <Data>provider specific data here</Data>    </Provider>    <Provider Name="logical name here">         <Data>provider specific data here</Data>    </Provider></AlternateDownloadSettings>
```

`AppXInplaceUpgradeEnabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Indicates whether Windows app package (.appx files) in-place upgrade is enabled.

`Enabled` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the agent is enabled.

`EvaluationSchedule` Data type: `String`

Access type: Read/Write

Qualifiers: none

Evaluation schedule for deployments.

## Remarks

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
