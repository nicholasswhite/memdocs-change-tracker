---
title: "Configuration Manager Server Runtime Requirements"
description: Microsoft Configuration Manager server applications that are developed by using the Configuration Manager SDK, have the following runtime requirements.
ms.date: "2017-03-14T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/7696cda6-0510-47f6-8302-71bb5d2e28cf
- https://authoring-docs-microsoft.poolparty.biz/devrel/bcbcbad5-4208-4783-8035-8481272c98b8
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/69c76c32-967e-4c65-b89a-74cc527db725
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Configuration Manager Server Runtime Requirements

Microsoft Configuration Manager server applications that are developed by using the Configuration Manager SDK, have the following runtime requirements.

## Managed Code

- A supported version of Windows Server as defined in [Supported operating systems for Configuration Manager site system servers](../../../core/plan-design/configs/supported-operating-systems-for-site-system-servers.md). For more information, see [General Requirements](#general-requirements).
- Installed Configuration Manager site server
- Microsoft.ConfigurationManagement.ManagementProvider .NET Framework assembly
- Microsoft .NET Framework version 4

## Configuration Manager Console User Interface Extension

Programming Configuration Manager console extensions has the following requirements:

- Installed Configuration Manager site server
- Installed Configuration Manager console
- .NET Framework 4.0

  For more information, see [About console extensions](../servers/console/about-configuration-manager-console-extension.md).

## VBScript

- Installed Configuration Manager site server
- Windows Script Host

## Windows 64-Bit Support

A 32-bit compiled application that uses Configuration Manager SDK interfaces to access Configuration Manager client or Configuration Manager server functionality works when it runs in 32-bit emulation on a 64-bit Windows operating system. However, a 64-bit compiled application that uses Configuration Manager SDK interfaces that access 32-bit Configuration Manager client or Configuration Manager server functionality does not work. Similarly, Configuration Manager SDK scripts do not work when the scripting host is a native 64-bit application. A Configuration Manager SDK script does work if it is called from within a 32-bit scripting host.

## General Requirements

> [!IMPORTANT]
>
> For more information about general Configuration Manager requirements, see [Supported configurations for Configuration Manager](../../../core/plan-design/configs/supported-configurations.md).

## See Also

[About console extensions](../servers/console/about-configuration-manager-console-extension.md) [Configuration Manager Client Development Requirements](client-development-requirements.md) [Configuration Manager Server Development Requirements](server-development-requirements.md)
