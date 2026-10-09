---
title: "SMS_EndpointProtectionAgentConfig Server WMI Class"
description: An SMS Provider server class that specifies the settings for the Endpoint Protection client.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/aa9d0281-4c35-44bb-8c75-a0920bde2014
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/c7449412-70b0-48ea-831f-3b132eafb97e
---

# SMS_EndpointProtectionAgentConfig Server WMI Class

The `SMS_EndpointProtectionAgentConfig` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in Configuration Manager, that specifies the settings for the Endpoint Protection client.

The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.

## Syntax

```
Class SMS_EndpointProtectionAgentConfig : SMS_ClientAgentConfig_BaseClass
{
    UInt32 AgentID;
    Boolean DisableFirstSignatureUpdate;
    Boolean EnableBlueProvider;
    Boolean EnableEP;
    UInt32 ForceRebootPeriod;
    UInt32 InstallRetryPeriod;
    Boolean InstallSCEPClient;
    Boolean LicenseAgreed;
    Boolean OverrideMaintenanceWindow;
    Boolean PersistInstallation;
    UInt32 PolicyEnforcePeriod;
    Boolean Remove3rdParty;
    Boolean SuppressReboot;
};
```

## Methods

The `SMS_EndpointProtectionAgentConfig` class doesn't define any methods.

## Properties

`AgentID` Data type: `UInt32`

Access type: Read-only

Qualifiers: [key, read]

Identifies the client agent component. The Endpoint Protection Agent ID is 20.

`DisableFirstSignatureUpdate` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Disable the first signature update on client from a remote source (Windows Update, WSUS, or UNC Path).

`EnableBlueProvider` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the Windows R2 provider is enabled. This value isn't visible/available in the console. The default value is `true`.

`EnableEP` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the agent is enabled.

`ForceRebootPeriod` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Pending reboot window in hours.

`InstallRetryPeriod` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Client-side verify common client existence interval.

`InstallSCEPClient` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the client agent will install the common client.

`LicenseAgreed` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if the Endpoint Protection License Agreement is approved.

`OverrideMaintenanceWindow` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if maintenance windows shouldn't be respected.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

`PersistInstallation` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

`true` if. EndPoint Protection should be installed on persisted storage. This only applied to embedded operating systems.

This information applies to System Center 2012 Configuration Manager SP1 or later, and System Center 2012 R2 Configuration Manager or later.

`PolicyEnforcePeriod` Data type: `UInt32`

Access type: Read/Write

Qualifiers: none

Client-side enforce anti-malware policy interval.

`Remove3rdParty` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Remove existing 3rd party anti-malware solution when the Endpoint Protection client installs.

`SuppressReboot` Data type: `Boolean`

Access type: Read/Write

Qualifiers: none

Suppress potential reboot after Endpoint Protection client installation.

## Remarks

Enabling the Endpoint Protection client may uninstall existing antivirus solutions. The Endpoint Protection client can't be enabled until an Endpoint Protection role is added to the hierarchy.

## Requirements

## Runtime Requirements

For more information, see [Configuration Manager Server Runtime Requirements](../../../../core/reqs/server-runtime-requirements.md).

## Development Requirements

For more information, see [Configuration Manager Server Development Requirements](../../../../core/reqs/server-development-requirements.md).
