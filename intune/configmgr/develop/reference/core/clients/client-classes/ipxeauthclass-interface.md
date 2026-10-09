---
title: IPxeAuthClass Interface
description: The IPxeAuthClass automation interface enables configuration of a PXE service point.
ms.date: "2016-09-20T00:00:00Z"
ms.subservice: sdk
ms.topic: reference
ms.collection: tier3
ms.service: configuration-manager
author: sccmavenger
cmProducts:
- https://authoring-docs-microsoft.poolparty.biz/devrel/43093068-2dda-408b-b3fe-dfd705c84f78
- https://authoring-docs-microsoft.poolparty.biz/devrel/97159432-14a9-4307-a469-d2f2c75f0e33
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
- https://authoring-docs-microsoft.poolparty.biz/devrel/50565c62-5f6b-4687-be38-323113c72c2e
- https://authoring-docs-microsoft.poolparty.biz/devrel/e453d60d-ba7e-43bc-8028-ec38e6b62512
---

# IPxeAuthClass Interface

The `IPxeAuthClass` automation interface, in Configuration Manager, enables configuration of a PXE service point by serializing certificate information in the form that is required for the [SubmitRegistrationRecord Method in Class SMS_Site](../../servers/configure/submitregistrationrecord-method-in-class-sms_site.md). This interface inherits from `IDispatch`.

## In This Section

| Term | Definition |
| --- | --- |
| [IPxeAuthClass::CreateIdentity Method](ipxeauthclass--createidentity-method.md) | Creates a PXE certificate identity used in the client configuration file. |
| [IPxeAuthClass::ReadIdentity Method](ipxeauthclass--readidentity-method.md) | Reads a PXE certificate identity from the client configuration file. |

## Remarks

The UUID for `IPxeAuthClass` is 2BCF9AFE-C441-4f69-A943-08A4C4EAAE5B.

## See Also

[PxeAuthClass Client COM Automation Class](pxeauthclass-client-com-automation-class.md) [About Operating System Deployment Site Role Configuration](../../../../osd/about-operating-system-deployment-site-role-configuration.md)
