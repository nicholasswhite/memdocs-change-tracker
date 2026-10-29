---
title: "Configuration Manager SDK libraries"
description: Use Configuration Manager libraries when you write unmanaged applications.
ms.date: "2021-11-18T00:00:00Z"
ms.subservice: sdk
ms.topic: article
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
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
- https://microsoft-devrel.poolparty.biz/DevRelOfferingOntology/6a8c83be-f1de-4e90-bde0-bd097999a60c
---

# Configuration Manager SDK libraries

In Configuration Manager, when you write unmanaged applications, you might have to include one or more of the following libraries. Use COM Interoperability to access COM objects from .NET Framework applications.

| Library | Description |
| --- | --- |
| ismifcom.dll | Contains a class wrapper for the install status MIF functions. Visual Basic and scripting programmers use this ActiveX control to create a status MIF file.   Visual Basic users must select the ISMIFCOM 1.0 Type Library project reference. Scripting users create this object by using "ISMIFCOM.InstallStatusMIF". |
| Microsoft.ConfigurationManager.Messaging.dll | Contains A .NET assembly encapsulating the client SDK that has an object model and transport for communicating with Configuration Manager site server roles such as the management point. |
| smsmsgapi.dll | Contains management point interface libraries. |
| smsrsgen.dll | Contains the Discovery Data Record functions. This DLL must exist in the directory from where you start your application. |
| smsrsgenctl.dll | Contains a class wrapper for the Discovery Data Record Functions. Visual Basic and scripting programmers use this control to create discovery data records. |

> [!NOTE]
>
> The library files are available as [NuGet packages](https://www.nuget.org/profiles/ConfigurationManagerTeam).

For more information about general Configuration Manager requirements, see [Supported configurations](../../../core/plan-design/configs/supported-configurations.md).
